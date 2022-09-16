<template>
<div class="btn"
>
  <slot name="icon"></slot>
  <slot name="text"></slot>

</div>
</template>

<script>

</script>

<style scoped lang="scss">
  .btn {
    display: inline-block;
    padding: 15px;
    margin: 5px;
    border-radius: 10px;
    background-color: orange;
  }

</style>