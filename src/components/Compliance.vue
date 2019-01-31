<template>
  <div class="hello">
    <h2>Compliance Requirements</h2>
    <ul v-if="reqs && reqs.length">
      <li v-for="(req, index) in reqs" :key="index">
        <div>
          <span v-if="req.status === 'true'"
            ><i class="material-icons">check_box</i></span
          >
          <span v-else
            ><i class="material-icons"> check_box_outline_blank</i></span
          >
          {{ req.title }}
        </div>
      </li>
    </ul>

    <ul v-if="errors && errors.length">
      <li v-for="(error, index) in errors" :key="index">{{ error.message }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Compliance",
  data() {
    return {
      msg: "Welcome to Your Vue.js App",
      reqs: [
        { id: 1, title: "Animal User Training", status: "false" },
        { id: 2, title: "Biosafety Training", status: "true" },
        { id: 3, title: "Research Ethics", status: "true" },
        { id: 4, title: "Research Security", status: "false" }
      ],
      errors: []
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello {
  max-width: 300px;
  margin: auto;
}
li {
  border: none;
  width: 300px;
  text-align: left;
}
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>

