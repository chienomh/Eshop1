/* MENU */
// CreatedBy: TDCHIEN 13/06/2021

<template>
  <div class="sidebar">
      <img src="../assets/icon/Logo_Full_White.png" alt="">
      <div class="menu">
        <div tabindex="1" class="tong_quan style_item"  
        >Tổng quan</div>
        <div  class="bao_cao style_item">Báo cáo</div>
        <div  class="don_hang style_item">Đơn hàng</div>
        <div  class="mua_hang style_item">Mua hàng</div>
        <div  class="khuyen_mai style_item">Khuyến mãi</div>
        <div  class="quan_ly_cua_hang style_item">Quản lý cửa hàng</div>
        <div  class="hang_hoa style_item">Hàng hoá</div>
      </div>
  </div>
</template>

<script>

export default {
  data() {
    return {
      
    };
  },

}
</script>

<style scoped>

    *{
      margin: 0px;
      padding: 0px;
    }
    .sidebar {
        margin: 0px;
        padding: 0px;
        width: 150px;
        height: 100%;
        background-color: #026b97;
        box-sizing: border-box;
    }

    /* Logo MISA Eshop */
    .sidebar img {
      width: 150px;
      background-color: #00577b;
    }

    .menu {
      margin-top: -4px;
    }

    /* Style ỉtem Menu */
    .menu .style_item{
      color: #FFFFFF;
      font-family: Text-Regular;
      font-size: 13px;
      height: 40px;
      line-height: 40px;
      padding-left: 40px;
      cursor: pointer;
      background-repeat: no-repeat;
      background-position: 9% 45%;
    }

    /* Icon item Menu */
    .menu .tong_quan {
      background-image: url("../assets/icon/TongQuan.png");    
    }
    .menu .bao_cao {
      background-image: url("../assets/icon/BaoCao.png");      
    }
    .menu .don_hang {
      background-image: url("../assets/icon/DonHang.jpg");     
    }
    .menu .mua_hang {
      background-image: url("../assets/icon/MuaHang.png");    
    }
    .menu .khuyen_mai {
      background-image: url("../assets/icon/KhuyenMai.png");     
    }
    .menu .quan_ly_cua_hang {
      background-image: url("../assets/icon/QuanLyCuaHang.png");    
    }
    .menu .hang_hoa {
      background-image: url("../assets/icon/HangHoa.png");
    }
    .style_item:hover {
        background-color: #00577b;
    }

    .quan_ly_cua_hang{
      background-color: #00577b;
    }
</style>
