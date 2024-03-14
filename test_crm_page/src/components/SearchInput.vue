<template>
  <div class="search-container">
    <img :src="getImgUrl(image)" class="user-container__img" />
  </div>
</template>

<script>
export default {
  props: {
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

<style lang="scss" scoped></style>
