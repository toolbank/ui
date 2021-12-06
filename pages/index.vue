<template>
  <div>
    <div class="space_60" />
    <div class="hero_lg">
      <p class="title">a</p>
      <p class="subtitle">a</p>
    </div>
    <div class="container">
      <h1>Hello World</h1>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.container{
  margin-left: 2vw;
  margin-right: 2vw;
}
.hero_lg{
  background-color: #96badb;
  padding: 4vw;
  display: flex;
  flex-flow: column;
  line-height: 0;
  .title {
    font-size: 2em;
    font-weight: 700;
  }
  .subtitle {
    font-size: 1.5em;
    font-weight: 400;
  }
}
</style>
