<template>
    <div class="main-store">
        <!-- <FormDelete class="formDelete"/> -->
        <div class="grid_table">
            <div class="action">
                <div class="add style_action" @click="openForm" >Thêm mới</div>
                <div class="replica style_action" @click="openForm">Nhân bản</div>
                <div class="edit style_action" @click="openForm">Sửa</div>
                <div class="delete style_action" @click="openAlert">Xóa</div>
                <div class="reload style_action">Nạp</div>
            </div>
            <div class="table_view">
                <table>
                    <thead>
                        <tr class="field_main">
                            <th style="min-width:50px; width:160px">Mã của hàng</th>
                            <th style="min-width:70px; width:249px">Tên cửa hàng</th>
                            <th style="min-width:100px;" >Địa chỉ</th>
                            <th style="min-width:60px; width:150px">Số điện thoại</th>
                            <th style="min-width:70px; width:150px">Trạng thái</th>
                        </tr>
                        <tr>
                            <th><div class="container"><span>*</span><input type="text"></div></th>
                            <th><div class="container"><span>*</span><input type="text"></div></th>
                            <th><div class="container"><span>*</span><input type="text"></div></th>
                            <th><div class="container"><span>*</span><input type="text"></div></th>
                            <th><div class="container"><input type="text" value="Đang hoạt động"><span><img src="../assets/icon/icon-down.png" alt=""></span></div></th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td class="style_content">1</td>
                            <td class="style_content">Circle K</td>
                            <td class="style_content">162 Mai Dịch, Hà Nội</td>
                            <td class="style_content">0123456789</td>
                            <td class="style_content">Đang hoạt động</td>
                        </tr>
                        <tr>
                            <td class="style_content">1</td>
                            <td class="style_content">Circle K</td>
                            <td class="style_content">162 Mai Dịch, Hà Nội</td>
                            <td class="style_content">0123456789</td>
                            <td class="style_content">Đang hoạt động</td>
                        </tr>
                        <tr>
                            <td class="style_content">1</td>
                            <td class="style_content">Circle K</td>
                            <td class="style_content">162 Mai Dịch, Hà Nội</td>
                            <td class="style_content">0123456789</td>
                            <td class="style_content">Đang hoạt động</td>
                        </tr>
                        <tr>
                            <td class="style_content">1</td>
                            <td class="style_content">Circle K</td>
                            <td class="style_content">162 Mai Dịch, Hà Nội</td>
                            <td class="style_content">0123456789</td>
                            <td class="style_content">Đang hoạt động</td>
                        </tr>
                        <tr>
                            <td class="style_content">1</td>
                            <td class="style_content">Circle K</td>
                            <td class="style_content">162 Mai Dịch, Hà Nội</td>
                            <td class="style_content">0123456789</td>
                            <td class="style_content">Đang hoạt động</td>
                        </tr>
                        <tr>
                            <td class="style_content">1</td>
                            <td class="style_content">Circle K</td>
                            <td class="style_content">162 Mai Dịch, Hà Nội</td>
                            <td class="style_content">0123456789</td>
                            <td class="style_content">Đang hoạt động</td>
                        </tr>
                        <tr>
                            <td class="style_content">1</td>
                            <td class="style_content">Circle K</td>
                            <td class="style_content">162 Mai Dịch, Hà Nội</td>
                            <td class="style_content">0123456789</td>
                            <td class="style_content">Đang hoạt động</td>
                        </tr>
                        <tr>
                            <td class="style_content">1</td>
                            <td class="style_content">Circle K</td>
                            <td class="style_content">162 Mai Dịch, Hà Nội</td>
                            <td class="style_content">0123456789</td>
                            <td class="style_content">Đang hoạt động</td>
                        </tr>

                    </tbody>
                </table>
            </div>
            <div class="footer">
                <div class="footer-left">
                    <div class="first-page style-icon-footer">
                        <img src="../assets/icon/firstPage.png" alt="">
                    </div>
                    <div class="prev style-icon-footer">
                        <img src="../assets/icon/prevPage.png" alt="">
                    </div>
                    <span style="margin: 16px 4px">Trang</span>
                    <input type="text" value="1" style="margin: 13px 3px">
                    <span style="margin: 16px 4px">trên 1</span>
                    <div class="last-page style-icon-footer">
                        <img src="../assets/icon/nextPage.png" alt="">
                    </div>
                    <div class="prev style-icon-footer">
                        <img src="../assets/icon/EndPage.png" alt="">
                    </div>
                    <div class="reload style-icon-footer" style="padding:2px;">
                         <img src="../assets/icon/HoiCham.jpg" alt="">
                    </div>
                    <select name="pages" id="pages">
                        <option value="10">10</option>
                        <option value="15">15</option>
                        <option value="50" selected=true>50</option>
                        <option value="100">100</option>
                    </select>
                </div>
                <div class="footer-right">
                    <span>Hiển thị 1 - 11 trên 11 kết quả</span>
                </div>
            </div>
        </div>
    </div>    
</template>

<script>

export default {

    components: {
        // FormDelete,
    },

    methods: {

        // Nhờ cha mở form
        openForm(){
            this.$emit("showFormNow")
        },

        // Nhờ cha mở alert thông báo xoá
        openAlert() {
            this.$emit("openAlertNow")
        },
    }
}
</script>
  
<style scoped>

    .formDelete {
        position: absolute;
        z-index: 3;
        width: 100%;
        height: 100%;
    }

    .main-store {
        height: calc(100vh - 52px);
        background-color: #e5e6eb;
        padding: 9px;
        box-sizing: border-box;
        position: relative;
    }

    .grid_table {
        position: relative;
        height: 100%;
        background-color: #FFFFFF;
        width: 100%;
        z-index: 2;
    }

    .grid_table .action {
        background-color: #026b97;
        width: 100%;
        height: 36px;
        cursor: pointer;
        display: flex;
    }

    .style_action {
        height: 100%;
        line-height: 36px;
        padding-left: 25px;
        padding-right: 7px;
        background-position: 3% 50%;
        color: #FFFFFF;
        border-right: 1px solid #00577b;
    }

    .action .add {
        background-image: url("../assets/icon/ThemMoi.png");
        background-repeat: no-repeat;
    }

    .action .replica {
        background-image: url("../assets/icon/NhanBan.png");
        background-repeat: no-repeat;
    }

    .action .edit {
        background-image: url("../assets/icon/Sua.png");
        background-repeat: no-repeat;
    }

    .action .delete {
        background-image: url("../assets/icon/Xoa.png");
        background-repeat: no-repeat;
    }

    .action .reload {
        background-image: url("../assets/icon/Nap.png");
        background-repeat: no-repeat;
    }

    .action .add:hover {
        background-color: #0088c1;
    }
    .action .replica:hover {
        background-color: #0088c1;
    }
    .action .edit:hover {
        background-color: #0088c1;
    }
    .action .delete:hover {
        background-color: #0088c1;
    }
    .action .reload:hover {
        background-color: #0088c1;
    }

    /* table */
    .table_view {
        width: 100%;
        max-height: calc(100vh - 160px);
        overflow: scroll;
    }

    table {
        width: 100%;
        border-collapse: collapse;
        overflow: scroll;
        cursor: pointer;
    }

    table th,td {
        height: 32px;
        border: 1px solid #d0d0d0;
        /* overflow: hidden; */
    }

    table tbody tr:hover {
        background-color:#d1f1ff;
    }

    table thead tr:nth-child(even) {
        background-color: #FFFFFF;
    }

    table thead tr:nth-child(odd) {
        background-color: #f0f0f0;
    }

    table thead{
        position: sticky;
        top: 0;
    }


    table tbody tr:nth-child(odd) {
        background-color: #FFFFFF;
    }

    table tbody tr:nth-child(even) {
        background-color: #f0f0f0;
    }

    table tbody tr:hover{
        background-color: #d1f1ff;
    }

    .container {
        display: flex;
    }

    .container span {
        width: 34px;
        line-height: 32px;
        cursor: pointer;
        border-right: 1px solid #d0d0d0;
    }
    .container input {
        border: none;
        border-left: 1px soli #d0d0d0;
        width: 100%;
        padding: 5px 10px;
    }

    .container input:focus {
        outline: none !important;
        border:1px solid #0088c1;
        box-shadow: 0 0 10px #719ECE;
    }

    .container img {
        width: 10px;
    }

    .style_content {
        padding: 7px 10px 6px;
    }
    
    .footer {
        position: absolute;
        bottom: 0;
        width: 100%;
        height: 52px;
        border: 1px solid #d0d0d0;
        display: flex;
    }

    .footer-left {
        display: flex;
        /* line-height: 52px; */
        color: #4B4C4C;
     
    }
    
    .style-icon-footer {
        margin-top: 13px;
    }

    .style-icon-footer {
        width: 24px;
        height: 24px;
        border: 1px solid #d0d0d0;
        margin-left: 3px;
        border-radius: 4px;
    }

    .footer-left input {
        height: 24px;
        width: 48px;
        text-align: center;
    }
    
    .footer-left select {
        width: 46px;
        height: 24px;
        border: 1px solid #9e9e9e;
        margin: 13px 2px;
        border-radius: 4px;    
    }

    .footer-right{
        position: absolute;
        right: 20px;
        line-height: 52px;
    }
</style>