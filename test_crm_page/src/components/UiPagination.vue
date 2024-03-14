<template>
  <div class="pagination">
    <div class="container">
      <span class="arrow-left"></span>
      <div class="number-container">
        <span>1</span>
        <span class="num-two">2</span>
        <span>3</span>
        <span>...</span>
        <span>12</span>
      </div>
      <span class="arrow-right"></span>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    totalPages: {
      type: Number,
      required: false,
    },
    currentPage: {
      type: Number,
      require: false,
    },
    sizePage: {
      type: Number,
      required: false,
    },
  },
};
</script>

<style lang="scss" scoped>
.pagination {
  background: #fff;
  border-radius: 12px;
  height: 68px;
  margin-top: 28px;
  cursor: pointer;
  .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 236px;
    height: 36px;
    padding: 14px 16px 14px 16px;
    .number-container {
      display: flex;
      justify-content: center;
      align-items: center;
      span {
        display: flex;
        align-content: center;
        justify-content: center;
        flex-wrap: wrap;
        width: 36px;
        height: 36px;
        font-family: Commissioner;
        font-weight: 400;
        font-size: 14px;
        line-height: 20px;
        color: rgba(133, 145, 174, 1);
      }
      .num-two {
        background-color: rgba(245, 247, 251, 1);
        color: #000;
        border-radius: 12px;
      }
    }
    .arrow-left {
      width: 20px;
      height: 20px;
      background-image: url("../assets/img/arrow_left.png");
    }
    .arrow-right {
      width: 20px;
      height: 20px;
      background-image: url("../assets/img/arrow_right.png");
    }
  }
}
</style>
