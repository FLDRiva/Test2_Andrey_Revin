<template>
  <div id="app" class="app">
    <div>
      <side-bar />
    </div>
    <div class="app__content">
      <head-top />
      <div class="app__container">
        <team-info />
        <ui-button />
        <ui-table />
        <ui-pagination />
      </div>
    </div>
  </div>
</template>

<script>
import SideBar from "../src/components/SideBar";
import HeadTop from "../src/components/HeadTop.vue";
import TeamInfo from "../src/components/TeamInfo";
import UiButton from "../src/components/UiButton";
import UiTable from "../src/components/UiTable";
import UiPagination from "../src/components/UiPagination";
export default {
  name: "App",
  components: {
    SideBar,
    HeadTop,
    TeamInfo,
    UiButton,
    UiTable,
    UiPagination,
  },
};
</script>

<style lang="scss">
@import "../src/style/reset";
@import "../src/style/text";
.app {
  background: #eff4fc;
  display: flex;
  flex-direction: row;

  &__content {
    height: 100vh;
    overflow: hidden;
  }

  &__container {
    height: calc(100vh - 76px);
    overflow: hidden;
    padding: 28px;
    position: relative;
    box-sizing: border-box;
  }
}
</style>
