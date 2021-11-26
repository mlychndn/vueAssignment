<template>
  <div class="bio">
    <h2>{{ name }}</h2>
    <h3>{{ age }}</h3>
  </div>
</template>

<script>
export default {
  props: ["name", "age"],
  data() {
    return {};
  },
};
</script>

<style>
body {
  background-color: rgb(9, 9, 70);
  color: white;
  text-align: center;
}
.bio {
  border: 1px solid white;
  border-radius: 10px;
  padding: 1rem;
  margin: auto;
  margin-top: 2rem;
  width: 35%;
  background-color: rgb(158, 158, 19);
}
</style>
