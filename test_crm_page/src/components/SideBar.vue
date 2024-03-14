<template>
  <div class="container_main">
    <div class="logo_menu">
      <div class="logo">
        <img src="../images/Vector.png" />
      </div>
      <router-link to="/">
        <img src="../images/2.png" />
      </router-link>
      <div>
        <img src="../images/3.png" />
      </div>
      <div>
        <img src="../images/4.png" />
      </div>
      <div>
        <img src="../images/5.png" />
      </div>
      <div>
        <img src="../images/6.png" />
      </div>
      <div>
        <img src="../images/7.png" />
      </div>
      <div>
        <img src="../images/8.png" />
      </div>
      <div>
        <img src="../images/9.png" />
      </div>
      <div>
        <img src="../images/10.png" />
      </div>
    </div>
    <ui-invite />
  </div>
</template>

<script>
import UiInvite from "../components/UiInvite.vue";
export default {
  name: "SideBar",
  components: {
    UiInvite,
  },
};
</script>

<style lang="scss" scoped>
.container_main {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin: 0;
  background-color: white;
  border-radius: 23px 0 0 23px;
  height: 100vh;
  .logo_menu {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-direction: column;
    border-radius: 29px 0 0 0;
    padding: 28px 0 0 0;
    cursor: pointer;
    .logo {
      margin-bottom: 1vh;
    }
  }
}
</style>
