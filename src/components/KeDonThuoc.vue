<template>
  <div class="prescriptions">
    <div class="prescriptions-Main">
      <div class="prescriptions-header">
        <div class="header-start d-flex flex-column">
          <p class="float-start mx-3 fw-bold ld-1 mb-1">Hiệu Thuốc An Tâm</p>
          <div class="info">
            <p>Địa chỉ: số 1 Phạm Văn Đồng-Cầu Giấy-Hà Nội</p>
            <p>Số điện thoại: 0123456789</p>
          </div>
        </div>
        <div class="header-end d-flex justify-content-end">
          <div class="cancel-btn rounded-circle" v-on:click.prevent="$parent.DisplayKeDonThuoc = true" >
            <i class="fa fa-times" aria-hidden="true"></i>
          </div>
        </div>
      </div>
      <div class="prescriptions-container">
        <h4 class="fw-bold col-12">ĐƠN THUỐC</h4>
        <div class="prescriptions-Content col-12">
          <div class="patient-info col-12">
            <div class="col-12 d-flex flex-wrap">
              <p class="col-4 text-start ps-3">Họ Tên: Vũ Văn Thắng</p>
              <p class="col-4 text-start ps-3">Ngày sinh: 10/04/2000</p>
              <p class="col-4 text-start ps-3">Giới Tính: Nam</p>
              <p class="col-4 text-start ps-3">Số Điện Thoại: 0123456789</p>
              <p class="col-8 text-start px-3">
                Địa chỉ: Số 1 Phạm Văn Đồng, Dịch Vọng Hậu, Cầu Giấy, Hà Nội
              </p>
              <p class="col-2 text-start ps-3">Chuẩn Đoán:</p>
              <textarea
                class="col-9 text-start ms-3"
                type="text"
                placeholder="Chuẩn đoán của bác sĩ..."
              ></textarea>
              <p class="col-4 text-start ps-3">Thuốc điều trị:</p>
              <table class="table table-bordered">
                <thead>
                  <tr>
                    <th scope="col" style="width: 10%">#</th>
                    <th scope="col" style="width: 60%">Tên Thuốc/Hàm lượng</th>
                    <th scope="col" style="width: 15%">ĐVT</th>
                    <th scope="col" style="width: 15%">Số Lượng</th>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <th scope="row">1</th>
                    <td><input class="col-12 my-input" type="text" /></td>
                    <td><input class="col-12 my-input" type="text" /></td>
                    <td><input class="col-12 my-input" type="text" /></td>
                  </tr>
                  <tr>
                    <td colspan="4">
                      <input
                        class="col-12 my-input ps-2"
                        type="text"
                        placeholder="Note..."
                      />
                    </td>
                  </tr>
                  <tr>
                    <th scope="row">2</th>
                    <td><input class="col-12 my-input" type="text" /></td>
                    <td><input class="col-12 my-input" type="text" /></td>
                    <td><input class="col-12 my-input" type="text" /></td>
                  </tr>
                  <tr>
                    <td colspan="4">
                      <input
                        class="col-12 my-input ps-2"
                        type="text"
                        placeholder="Note..."
                      />
                    </td>
                  </tr>
                  <tr>
                    <th scope="row">3</th>
                    <td><input class="col-12 my-input" type="text" /></td>
                    <td><input class="col-12 my-input" type="text" /></td>
                    <td><input class="col-12 my-input" type="text" /></td>
                  </tr>
                  <tr>
                    <td colspan="4">
                      <input
                        class="col-12 my-input ps-2"
                        type="text"
                        placeholder="Note..."
                      />
                    </td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>
        </div>
      </div>
      <div class="prescriptions-footer m-box-sizing">
        <div class="d-flex flex-row-reverse me-4 m-box-sizing w-100">
          <div class="float-end m-box-sizing col-4">
            <p class="mb-0">Ngày....Tháng....Năm.....</p>
            <p class="fontsize-07rem fw-bold">Bác Sĩ Điều Trị</p>
            <p class="pt-5 mt-5">Vũ Văn Thắng</p>
          </div>
          <div
            class="d-flex flex-column text-start m-box-sizing col-8 py-5 px-3"
          >
            <p class="fontsize-07rem">
              Bệnh nhân đi khám lần sau xin vui lòng mang theo đơn này!
            </p>
            <p>Lời dặn của bac sĩ: hết thuốc tái khám!</p>
          </div>
        </div>
        <div class="d-flex btn-group float-end pe-2 col-6" role="group" aria-label="Basic example">
          <button type="button" class="btn btn-primary col-2 m-3" v-on:click.prevent="$parent.DisplayKeDonThuoc = true" >send</button>
          <button type="button" class="btn btn-secondary col-2 m-3" v-on:click.prevent="$parent.DisplayKeDonThuoc = true" >cencal</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.prescriptions {
  display: flex;
  justify-content: center;
  position: absolute;
  width: 100%;
  height: 100%;
  z-index: 99;
  background-color: rgba(28, 32, 32, 0.11);
}
.prescriptions-Main {
  display: inline;
  width: 50%;
  height: 100%;
  background-color: rgb(255, 255, 255);
  overflow: hidden scroll;
}
.prescriptions-header {
  display: flex;

  width: 100%;
}
.header-start,
.header-end {
  width: 50% !important;
  padding: 0;
  margin: 0;
}
.info {
  font-size: 0.7rem;
  line-height: 0;
}

.cancel-btn {
  height: 35px;
  padding: 5px 10px;
  display: flex;
  justify-content: end;
  font-size: 1.5rem;
  color: gray;
}
.cancel-btn:hover {
  color: black;
  background-color: #f3f8fda2;
}

textarea {
  height: 120px;
  padding: 12px 20px;
  box-sizing: border-box;
  border: 2px solid #ccc;
  border-radius: 4px;
  /* background-color: #f8f8f8; */
  resize: none;
}
.my-input {
  border: none;
  line-height: 41.5px;
  margin: 0;
}
.my-input:focus-visible {
  border: none !important;
  outline: none;
  resize: both;
}
td {
  padding: 0 !important;
}
.prescriptions-footer {
  width: 100%;
}
</style>