<template>
  <div id="header bg-primary">
    <nav class="navbar navbar-expand-lg navbar-light bg-primary">
      <div class="container-fluid px-4">
        <a class="navbar-brand fs-3 text-white col-1" href="#"> AnTâm </a>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse col-8" id="navbarSupportedContent">
          <form class="d-flex col-11 ms-5">
            <input
              class="form-control ms-5 backgroung-input"
              type="search"
              placeholder="Tìm kiếm"
              aria-label="Search"
            />
            <button class="btn ms-1 bg-white" type="submit">
              <i
                class="fa fa-search fs-5"
                aria-hidden="true"
                title="Tìm kiếm"
              ></i>
            </button>
          </form>
        </div>
        <div class="collapse navbar-collapse col-3 justify-content-center" id="navbarSupportedContent">
          <button class="btn ms-1 bg-white" type="submit">
            <i class="fa fa-shopping-cart fs-5" aria-hidden="true"></i>
          </button>
          <button class="btn ms-1 bg-white" type="submit">
            <i class="fa fa-bell-o fs-5" aria-hidden="true"></i>
          </button>
          <button class="btn ms-1 bg-white" type="submit">
            <i class="fa fa-comment-o fs-5" title="Tin nhắn"></i>
          </button>
          <button class="btn ms-1 bg-white" type="submit">
            <i class="fa fa-sign-in fs-5" title="Đăng nhập/Đăng ký"></i>
          </button>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: "CompHeader",
  data() {
    return {
      messega: "My Name is Vu Van Thang",
    };
  },
  props: {
    mytext: String,
    mytext2: String,
  },
};
</script>

<style scoped>

</style>
