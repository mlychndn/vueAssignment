<template>
  <header><h1>Practicing on component!😃😃</h1></header>
  <user-data @add-list="addList"></user-data>
  <active-user
    v-for="detail in bio"
    :key="detail.id"
    :name="detail.name"
    :age="detail.age"
  ></active-user>
</template>

<script>
export default {
  data() {
    return {
      bio: [
        {
          id: "1234",
          name: "Malay Chandan",
          age: "28",
        },
        {
          id: "1236",
          name: "Suriya Ghosh",
          age: "26",
        },
      ],
    };
  },
  methods: {
    addList(name, age) {
      const newList = {
        id: new Date().toISOString(),
        name,
        age,
      };
      this.bio.push(newList);
    },
  },
};
</script>

<style>
body {
  margin: 0;
}
</style>
