<template>
  <h1 @click="increase">
    {{ count }} / {{ doubleCount}}
  </h1>
  <h1 @click="changeMessage">
    {{ message }} / {{reversedMessage}}
  </h1>
</template>

<script>
import { ref, computed,watch } from "vue";
export default {
  setup() {
    let count = ref(0);
    const doubleCount = computed(() => {
      return count.value * 2
    })
    function increase() {
      count.value += 1;
    }
    let message = ref("helllo world");
    const reversedMessage = computed(() => {
      return message.value.split('').reverse().join('')
    })

    watch(message,(newValue)=>{
      console.log(newValue)
    })

    function changeMessage() {
      message.value = "Good?!";
    }

    return {
      count,
      doubleCount,
      message,
      reversedMessage,
      increase,
      changeMessage,
    };
  },
};
</script>
