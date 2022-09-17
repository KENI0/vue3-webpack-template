<template>
  <h1 :style = "{color: 글자색}"> child : {{ msg.value}}</h1>
</template>

<script>
export default {
  inject: [ 'msg','글자색' ]

};
</script>
