<template>
  <section v-if="hasFruit > 0">
    <h1>Fruits</h1>
    <ul>
      <li v-for="fruit in fruits" :key="fruit">
        {{ fruit }}
      </li>
    </ul>
  </section>
  <section>
    <h1>reverseFruits</h1>
    <ul>
      <li v-for="fruit in reverseFruits" :key="fruits">
        {{ fruit }}
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  data() {
    return {
      fruits: ["apple", "banana", "orange"],
    };
  },
  computed: {
    hasFruit() {
      return this.fruits.length;
    },
    reverseFruits() {
      return this.fruits.map((fruit) => {
        return fruit.split("").reverse().join("");
      });
    },
  },
};
</script>

<style>
h1 {
  color: red;
}
</style>
