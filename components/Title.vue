<template>
<div class="container">
    <h2 class="title-h2">
        <slot></slot>
    </h2>
</div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
    .title-h2 {
      text-transform: uppercase;
      font-weight: bold;
      font-size: 30px;
      box-shadow: inset 4px 0px #ce922a;
      padding-left: 20px;
      margin: 50px 0px;
  }
</style>