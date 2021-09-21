<template>
  <div>
    <div class="ax-background position-fixed">
      <div class="ax-icon-seo1"></div>
      <div class="ax-icon-seo1"></div>
    </div>
    <div class="container-xl ax-inner my-xl-5">
      <div class="ax-inner-content">
        <axHeader />
        <Nuxt />
        <axFooter />
      </div>
    </div>
  </div>
</template>
<script>
import axHeader from "../components/axHeader.vue";
import axFooter from "../components/axFooter.vue";
export default {
  components: { axHeader, axFooter },
};
</script>
<style>
.page-enter-active,
.page-leave-active {
  transition: opacity 1.5s;
}
.page-enter,
.page-leave-to {
  opacity: 0;
}

.layout-enter-active,
.layout-leave-active {
  transition: opacity 0.1s;
}
.layout-enter,
.layout-leave-to {
  opacity: 0;
}
</style>
