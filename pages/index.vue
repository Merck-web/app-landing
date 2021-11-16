<template>
  <div class="index">
    <div class="container">
      <div class="ave">
        <Avetures />
      </div>
    </div>
    <div class="facts-section"><Facts /></div>
    <AppScreen />
  </div>
</template>

<script>
export default {};
</script>
<style lang="scss" scoped>
.ave {
  width: 100%;
}
.facts-section {
  background-color: var(--black-100);
}
</style>
