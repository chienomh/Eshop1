<template>
  <div class="main-delele">
    <div class="form-alert">
        <div class="title-alert">
            <span>Xóa dữ liệu</span>
            <span class="button-close">
                <img src="../assets/icon/cancel-gray.png" alt="" @click="closeAlert">
            </span>
        </div>
        <div class="main-title-alert">
            <div class="title-main-alert">
                <span>
                    Bạn có chắc chắn muốn xóa Circle K khỏi danh sách cửa hàng. 
                </span>
            </div>
        </div>
        <div class="active-alert">
            <div class="select-alert">
                <button class="confirm">Xóa</button>
                <button class="no" @click="closeAlert">Hủy bỏ</button>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    methods: {
        closeAlert() {
            this.$emit("closeAlertNow")
        }
    }
};
</script>

<style scoped>
.main-delele {
  width: 100%;
  height: 100vh;
  background-color: rgba(0, 0, 0, 0.4);
  display: flex;
}
.form-alert {
  width: 400px;
  height: 160px;
  background-color: #FFFFFF;
  margin: auto;
  border-radius: 4px;
}

.title-alert {
    background-color: #cfcfcf;
    border-radius: 4px;
    height: 40px;
    padding: 10px 17px;
    border-bottom: #d0d0d0;
    position: relative;
}

.title-alert span {
    font-size: 16px;
    font-weight: 700;
}

.main-title-alert {
    height: 60px;
    padding: 10px 10px 10px 70px;
    background-image: url("../assets/icon/confirm-blue.png");
    background-repeat: no-repeat;
    background-position: 5% 50%;
    border: 1px solid #d0d0d0;
}

.button-close{
    position: absolute;
    right: 10px;
    top: 13px
}

.button-close img {
    width: 16px;
}

.active-alert {
    height: 60px;
    line-height: 60px;
    position: relative;
}

.confirm {
    width: 75px;
    height: 32px;
    background-color: #eb7728;
    outline: none;
    border: none;
    border-radius: 3px;
    background-image: url("../assets/icon/Xoa.png");
    background-repeat: no-repeat;
    background-position: 5% 50%;
    color: #FFFFFF;
    font-weight: 500;
    cursor: pointer;

}

.confirm:hover {
    background-color: #f7904b;
}

.no {
    width: 90px;
    height: 32px;
    outline: none;
    border: none;
    border-radius: 3px;
    background-image: url("../assets/icon/cance-whtie.png");
    background-repeat: no-repeat;
    background-size: 14px;
    background-position: 5% 50%;
    color: #00577b;
    font-weight: 700;
    background-color: #FFFFFF;
    cursor: pointer;
    margin-left: 5px;

}

.select-alert {
    position: absolute;
    right: 0;
}

</style>