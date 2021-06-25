<template>
  <div id="app">
     <div class="main">
        <SiderBar/>
        <div class="right">
          <Header/>
          <StoreCatalog @showFormNow="isShowForm"
          @openAlertNow="isShowAlert"
          />
        </div>
     </div>
     <div class="form_detail" v-if="isHidden">
        <Form @closeFormNow="isCloseForm"/>
     </div>
    <FormDelete class="form_delete" 
      @closeAlertNow="isShowAlert" 
      v-if="isAlert"
    />
    <!-- <Autocomplete/> -->
  </div>
</template>

<script>
import SiderBar from '../src/views/SiderBar.vue'
import Header from '../src/views/Header.vue'
import StoreCatalog from '../src/views/StoreCatalog.vue'
import Form from '../src/views/Form.vue'
import FormDelete from '../src/views/FormDelete.vue'
// import Autocomplete from '../src/views/autocomplete.vue'


export default {
  components: {
    SiderBar,
    Header,
    StoreCatalog,
    Form,
    FormDelete,
    // Autocomplete
  },

  data() {
    return {
      isHidden : false,
      isAlert : false
    }
  },

  methods: {

    // sự kiện đóng mở form
    isShowForm() {
      this.isHidden = true;
    },
    isCloseForm(){
      this.isHidden = false
    },

    // Sự kiện đóng/mở alert
    isShowAlert() {
      this.isAlert = !this.isAlert
    },
  }
}
</script>

<style>

/* Reset page */
*{
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  font-family: Text-Regular;
  font-size: 13px;
}

#app {
  margin: 0px;
  padding: 0px;
  width: 100%;
  height: 100vh;
  display: flex;
}

.main {
  display: flex;
  flex: 1;
  position: relative;
}

.right {
  flex: 1;
}

.form_detail {
  position: absolute;
  z-index: 2;
  width: 100%;
  height: 100%;
}

.form_delete {
  position: absolute;
  z-index: 3;
  width: 100%;
  height: 100%;
}

</style>
