<template>
    <div id="header">
        <div class="title_header">
            Cửa hàng
        </div>
        <div class="main">
            <!-- Select box -->
            <select name="NameShop" id="shop">
                <option>Vinmart</option>
                <option>Vinmart 1</option>
                <option>Cir</option>
                <option>Circle K</option>
                <option>Misard</option>
                <option>Cinrale</option>
            </select>

            <!-- Account -->
            <div class="account">
                <img src="../assets/icon/default-avatar.jpg" alt="avatar">
                <span class="name_account">Nguyễn Văn Mạnh</span>
                <img src="../assets/icon/icon-down.png" id="icon_down">
            </div>

            <!-- Action -->
            <div class="action">
                <div class="icon_dien_thoai">
                    <img src="../assets/icon/DienThoai.png" alt="">
                </div>
                <div class="icon_chuong style_action">
                    <img src="../assets/icon/Chuong.png" alt="">
                </div>
                <div class="icon_help style_action">
                    <img src="../assets/icon/HoiCham.jpg" alt="">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
    #header {
        height: 52px;
        display: flex;
        position: relative;
    }

    #header .title_header {
        width: 150px;
        font-family: Text-Bold;
        font-size: 18px;
        font-weight: 700;
        line-height: 52px;
        padding-left: 20px;
    }

    .main {
        display: flex;
        align-items: center;
        justify-content: center;
        flex: 1;
        justify-content: flex-end;
    }

    /* Style input */
    .main #shop {
        width: 200px;
        height: 38px;
        border-radius: 4px;
        display: flex;
    }

    .account {
        display: flex;
        align-items: center;
        height: 100%;
        cursor: pointer;
    }

    .account img {
        width: 30px;
        margin-right: 5px;
        margin-left: 10px;
    }
    
    .account #icon_down{
        width: 12px;
    }

    .name_account {
        font-family: Text-Regular;
        font-weight: 700;
        font-size: 13px;
    }

    .action {
        display: flex;
        align-items: center;
        justify-content: center;
        cursor: pointer;
    }

    .icon_dien_thoai {
        background-color: #00577b;
    }

    .style_action {
        width: 45px;
        height: 50px;
        text-align: center;
        line-height: 50px;
    }
    .icon_chuong {
        border-right: 1px solid #bbbbbb;
    }
</style>