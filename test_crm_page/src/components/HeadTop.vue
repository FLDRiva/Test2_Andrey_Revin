<template>
  <div class="container">
    <div class="one-team-ellements">
      <div class="gradient_block"></div>
      <burger-menu />
      <span>Team</span>
    </div>
    <div class="top_bar">
      <search-input />
      <span>
        <img src="../images/Notification.png" />
      </span>
      <span class="line"></span>
      <user-info :image="'image_1.png'" />
      <span class="frame_text">Ernest Eberly</span>
      <user-info :label="'Ernest'" />
      <span class="arrow">
        <img src="../images/Arrow.png" />
      </span>
    </div>
  </div>
</template>

<script>
import BurgerMenu from "../components/BurgerMenu.vue";
import SearchInput from "../components/SearchInput.vue";
import UserInfo from "../components/UserInfo.vue";
export default {
  name: "HeadTop",
  components: {
    BurgerMenu,
    SearchInput,
    UserInfo,
  },
};
</script>

<style lang="scss" scoped>
.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: #fff;
  width: 100%;
  height: 76px;
  .one-team-ellements {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 28px;
    font-family: Commissioner;
    font-weight: 500;
    font-size: 22px;
    line-height: 33px;
    .gradient_block {
      width: 28px;
      height: 76px;
      background: linear-gradient(
        90deg,
        rgba(42, 53, 90, 0.04) 0%,
        rgba(42, 53, 90, 0) 100%
      );
    }
  }
  .top_bar {
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: Commissioner;
    font-weight: 500;
    size: 14px;
    gap: 28px;
    img {
      width: 24px;
      height: 24px;
    }
    .line {
      width: 32px;
      border: 1px solid rgba(229, 232, 239, 1);
      transform: rotate(-90deg);
    }
    .arrow {
      width: 20px;
      height: 20px;
      margin-right: 20px;
    }
  }
}
</style>
