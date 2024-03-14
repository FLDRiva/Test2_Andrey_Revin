<template>
  <div class="burger-container">
    <div class="line1"></div>
    <div class="line1"></div>
    <div class="line1"></div>
  </div>
</template>

<script>

</script>

<style lang="scss" scoped>
  .burger-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 5px;
  }
  .line1 {
    width: 16px;
    height: 1px;
    background-color: rgba(42, 53, 90, 1);
  }
</style>