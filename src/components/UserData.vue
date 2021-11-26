<template>
  <form class="form" action="submit" @submit.prevent="submitForm()">
    <div class="input">
      <label for="name">Name:</label>
      <input type="text" v-model="inputName" />
    </div>
    <div class="input">
      <label for="name">Age:</label>
      <input type="text" v-model="inputAge" />
    </div>
    <div>
      <button type="submit">Add User</button>
    </div>
  </form>
</template>

<script>
export default {
  data() {
    return {
      inputName: "",
      inputAge: "",
    };
  },
  methods: {
    submitForm() {
      console.log("Form is submitted!");
      this.$emit("add-list", this.inputName, this.inputAge, this.inputAge);
    },
  },
};
</script>

<style>
.form {
  border: 1px solid;
  border-radius: 10px;
  width: 35%;
  margin: auto;
  padding: 1rem;
  background-color: burlywood;
}

.input {
  padding: 0.2rem;
}
input {
  width: 50%;
  padding: 0.2rem;
  border-radius: 10px;
}
label {
  padding: 0.4rem;
  font-size: 120%;
}

button {
  padding: 0.2rem;
  width: 6rem;
  margin-top: 0.2rem;
  color: red;
  border-radius: 5px;
  background-color: blanchedalmond;
}
</style>
