<template>
  <hello @woo="클릭"
        @우영="출력"
  ></hello>
</template>

<script>
  import hello from '~/components/hello'
  export default {
    components: {
      hello 
    },
    methods: {
      클릭: function(event) {
        console.log('안녕!!')
        console.log(event)
      },
      출력(msg) {
        console.log(msg)
      }

  }
}
</script>