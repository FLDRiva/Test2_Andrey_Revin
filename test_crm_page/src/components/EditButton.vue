<template>
  <div class="button-container">
    <button>
      <img src="../assets/img/edit.jpg" />
      {{ label }}
    </button>
  </div>
</template>

<script>
export default {
  props: {
    label: {
      type: String,
      default: "",
    },
  },
  computed: {},
};
</script>

<style lang="scss" scoped>
.button-container {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 78px;
  height: 36px;
  button {
    display: flex;
    justify-content: center;
    align-items: center;
    border: none;
    background: transparent;
    border: 1px solid rgba(229, 232, 239, 1);
    border-radius: 7px;
    width: 78px;
    height: 36px;
    gap: 4px;
  }
}
</style>
