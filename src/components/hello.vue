<template>
<h1>click here!</h1>
<h2 @click="$emit('woo',$event)"> 안녕 ! </h2>
<h3>{{msg }} </h3>
<input type="text"
      v-model="msg"
      >
</template>

<script>
export default {
  data(){
    return{
      msg: ''
    }
  },
  emits: [
  'woo',
  '우영'
  ],
  watch: {
    msg() {
      this.$emit('우영',this.msg)
    }
  }
}
</script>