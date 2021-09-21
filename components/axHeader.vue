<template>
  <div
    class="navbar navbar-expand-lg ax-nav row d-flex justify-content-space-around align-items-center py-4"
  >
    <div
      class="col-6 mx-auto col-md-4 ax-nav-logo-section d-flex justify-content-start mr-4"
    >
      <div class="ax-nav-logo ax-icon-logo"></div>
    </div>
    <div class="col-2 d-md-none d-flex mx-auto col-md-4 ax-nav-logo-section">
      <div class="ax-nav-logo"></div>
    </div>

    <button
      class="col col-md-4 d-lg-none ax-menu-button btn collapsed"
      @click="ax_fixed_logo()"
    >
      <span class="ax-icon-menu"></span>
    </button>
    <div
      class="col-lg d-lg-flex justify-content-end collapse navbar-collapse ax-mobile"
      id="navbar"
      :class="myele"
    >
      <ul @click="ax_fixed_logo()" class="navbar-nav ax-list-desktop">
        <li class="nav-item">
          <NuxtLink to="/">درباره من</NuxtLink>
        </li>
        <li class="nav-item"><NuxtLink to="/about">رزومه</NuxtLink></li>
        <li class="nav-item"><NuxtLink to="/">نمونه‌کار‌ها</NuxtLink></li>
        <li class="nav-item"><NuxtLink to="/index2">بلاگ</NuxtLink></li>
        <li class="nav-item"><NuxtLink to="/">هزینه ها</NuxtLink></li>
        <li class="nav-item"><NuxtLink to="/">تماس</NuxtLink></li>
        <li class="nav-item">
          <NuxtLink to="/"><i class="ax-icon-search"></i></NuxtLink>
        </li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  transition: "home",
  mode: "out-in",
  data() {
    return {
      show: false,
      myele: null,
    };
  },
  methods: {
    ax_fixed_logo() {
      this.show = !this.show;
      console.info(this.show);
      if (this.show == false) {
        this.myele = null;
      } else {
        this.myele = "show";
      }
    },
  },
};
</script>
<style>
.ax-mobile.show {
  transition: 1s ease-in;
}
.ax-mobile {
  transition: 1s ease-in-out;
}
</style>
