<template>
  <div class="user-container">
    <img :src="getImgUrl(image)" class="user-container__img" />
    <span class="user-container__label">{{ label }}</span>
  </div>
</template>

<script>
export default {
  props: {
    label: {
      type: String,
      default: "",
    },
    image: {
      type: String,
      default: "",
    },
  },
  methods: {
    getImgUrl(img) {
      return require("../assets/img/" + img);
    },
  },
};
</script>

<style lang="scss" scoped>
.user-container {
  display: flex;
  justify-content: center;
  align-self: center;
  align-items: center;
  align-content: center;

  &__label {
    margin-left: 10px;
  }
}
</style>
