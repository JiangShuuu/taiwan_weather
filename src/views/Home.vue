<template>
  <div class="main">
    <div class="container">
      <div class="main_svg d-none">
        <Taiwan />
      </div>
      <div class="main_content">
        <Main />
      </div>
    </div>
  </div>
</template>

<script>
import Taiwan from "../components/taiwan.vue";
import Main from "../components/main.vue";

export default {
  components: {
    Taiwan,
    Main,
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/All.scss";
.main {
  @include flexCenter;
  background-color: $background_blue;
  height: 100vh;
  .container {
    width: 100%;
    @include flexCenter;
    @include pad {
      width: 90%;
    }
    @include web {
      width: 90%;
    }
    .main_svg {
      @include web {
        display: block;
        width: 40%;
      }
    }
    .main_content {
      width: 100%;
      height: 100%;
    }
  }
}
</style>
