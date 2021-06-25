<template>
  <div class="autocomplete">
    <div class="wrapper-input-quoc-gia">
      <input
        type="text"
        @keyup="getValue"
        v-model="valueSelectInput"
        class="style-input-small style-boder"
        @keydown="test"
      />
      <div class="keydown" @click="isShow">
        <img src="../assets/icon/icon-down.png" alt="" />
      </div>
    </div>
    <div class="wrapper" v-if="isShowList">
      <div
        class="list"
        v-for="(item, index) in this.searched"
        :key="index"
        @click="selectOption"
        @keyup.enter="selectOption"
        ref="test"
        :class="{ focus: index === focus }"
      >
        {{ item }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    data: Array,        
  },

  data() {
    return {
      customers: this.data,
      isShowList: false,
      searched: [],
      valueSelectInput: "",
      focus: null,
    };
  },

  methods: {
    getValue(e) {
      let dataInput = e.target.value;
      (this.searched = []),
        (this.searched = this.customers.filter(
          (x) => x.toUpperCase().indexOf(dataInput.toUpperCase()) > -1
        ));
      if (this.searched && dataInput) this.isShowList = true;
      else this.isShowList = false;
    },

    isShow() {
      this.searched = this.customers;
      this.focus = 0;
      this.isShowList = !this.isShowList;
    },

    selectOption(e) {     
      this.valueSelectInput = e.target.innerText;
      this.isShowList = false;
    },

    test: function (event) {
      switch (event.keyCode) {
        case 38:
          if (this.focus === null) {
            this.focus = 0;
          } else if (this.focus > 0) {
            this.focus--;
          }
          break;
        case 40:
          if (this.focus === null) {
            this.focus = 0;
          } else if (this.focus < this.searched.length - 1) {
            console.log(this.focus);
            this.focus++;
          }
          break;
        case 13:{
            this.isShowList = false;
        }
      }
    },
  },
};
</script>

<style scoped>
.autocomplete {
  width: 167px;
  height: 32px;
  position: relative;
}

.style-input-small {
  width: 137px;
  height: 32px;
}

.wrapper-input-quoc-gia {
  display: flex;
}

.nation {
  position: relative;
  width: 600px;
}

.wrapper {
  position: absolute;
  left: 105px;
  z-index: 5;
  border-radius: 5px;
  box-shadow: 1px 1px 3px black;
  max-height: 200px;
  overflow: hidden;
  overflow: scroll;
}

.keydown {
  border: 1px solid #d0d0d0;
  min-width: 30px;
  height: 32px;
  cursor: pointer;
  border-left: 0px;
  border-top-right-radius: 3px;
  border-bottom-right-radius: 3px;
  background-image: url("../assets/icon/icon-down.png");
  text-align: center;
  line-height: 35px;
}

.keydown img {
  width: 10px;
}

.list {
  background-color: white;
  width: 137px;
  cursor: pointer;
  height: 32px;
  line-height: 37px;
}

.list:hover {
  background-color: #0088c1;
  color: white;
}

div.focus {
  background-color: #0088c1;
  color: white;;
}

.style-boder {
  border: 1px solid #d0d0d0;
  border-top-left-radius: 3px;
  border-bottom-left-radius: 3px;
  padding-left: 10px;
}
</style>