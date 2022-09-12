<template>
  <ul>
<li v-for="{id, name} in 과일객체" :key="id">
  {{ name }}
</li>
</ul>
</template>

<script>
  import shortid from 'shortid'
  export default{
    data() {
      return{
      과일들 : ['딸기','포도','사과']
      }
    },
    computed: {
      과일객체() {
        return this.과일들.map(과일 => {
          return{
            id: shortid.generate(),
            name: 과일
          }
        })
      }
    }
  }

</script>