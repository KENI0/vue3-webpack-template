<!-- 양방향 데이터 바인딩 -->
<template>
  <h1> {{msg}}</h1>
<input type="text"
  @input="msg = $event.target.value"
>
<input type="checkbox"
    v-model="체크"
>
{{ 체크}}

</template>

<script>
  export default {
    data() {
      return {
        msg: "안녕!",
        체크: false
        
      }
    },
    }
  
</script>