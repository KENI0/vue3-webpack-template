<template>
  <Button>
    <template v-slot:text>
    <span>우영</span>
    </template>
    <template v-slot:icon>
    <span>WOO</span>
    </template>
  </Button>
</template>

<script> 
import Button from '~/components/Mybutton'
  export default {
    components: {
      Button
    }
  }
</script>