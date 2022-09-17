<template>
  <button @click="message = 'Good enough!'">
    click here!
  </button>

  <h1> app: {{message}}</h1>
  <Parent></Parent>

</template>

<script>
import Parent from "~/components/parent";
import { computed } from 'vue'
export default {
  components: {
    Parent,
  },
  data() {
    return {
      message: "hello!",
      글자색상: "orange",
    };
  },
  provide(){
    return{
      msg: computed(() => {
        return this.message 
      }),
    글자색: this.글자색상  
    }
  }
};
</script>
