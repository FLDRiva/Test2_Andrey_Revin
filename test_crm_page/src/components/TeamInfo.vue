<template>
  <div class="container">
    <div class="icon_text">
      <img src="../images/Frame 2084.png" />
      <div class="text_container">
        <span>Team</span>
        <img src="../assets/img/info.png" class="image" />
      </div>
    </div>
    <div class="members" v-for="item in objTeam" :key="item.number">
      <div class="number_of_mambers">
        <div class="number-text">
          <p>{{ item.number }}</p>
          <span>{{ item.text }}</span>
        </div>
        <span v-if="item.icon === 'ellapse'">
          <div class="ellapse"></div>
        </span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      objTeam: [
        { number: 130, text: "members", icon: "" },
        { number: 36, text: "online", icon: "ellapse" },
        { number: 50, text: "men", icon: "" },
        { number: 80, text: "women", icon: "" },
        { number: 29, text: "average age", icon: "" },
        { number: 265, text: "days work on avarage", icon: "" },
        { number: 36, text: "days work newest employee", icon: "" },
        { number: 1256, text: "days work oldest employee", icon: "" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.container {
  display: inline-flex;
  flex-direction: row;
  align-items: center;
  background: rgba(255, 255, 255, 1);
  width: auto;
  border-radius: 10px;
  gap: 50px;
  padding: 16px 28px 16px 28px;
  font-family: Commissioner;
  font-weight: 500;
  height: 79px;
  box-sizing: border-box;

  // @media (max-width: 1366px) {
  //   width: auto;
  // }
  .icon_text {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 16px;
    .text_container {
      display: flex;
      gap: 4px;
      position: relative;
    }
    .image {
      position: relative;
      top: -7px;
    }
    span {
      font-size: 14px;
      line-height: 20px;
    }
  }
  .number_of_mambers {
    display: flex;
    .number-text {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      @media (max-width: 1366px) {
        width: max-content;
      }
    }
    span {
      font-weight: 400;
      font-size: 12px;
      line-height: 18px;
      color: rgba(133, 145, 174, 1);
    }
    p {
      font-size: 22px;
      line-height: 28.6px;
    }
    .ellapse {
      width: 6px;
      height: 6px;
      border-radius: 50px;
      background-color: rgba(36, 193, 130, 1);
    }
  }
}
</style>
