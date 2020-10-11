<template>
  <div class="hello">
    <h1>Nuclear Helper</h1>
    <open-code v-for="(el, i) in codes" :key="i" />
    <button @click="newOpenCode">+</button>
  </div>
</template>

<script>
import openCode from "./search";

export default {
  components: {
    openCode
  },
  data() {
    return {
      codes: [""]
    };
  },
  methods: {
    newOpenCode() {
      this.codes.push("");
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
h1 {
  color: #718096;
  letter-spacing: 0.1em;
  font-weight: 300;
  font-size: 4rem;
}
input {
  margin: auto;
  margin-top: 0.25rem;
  border: solid;
  border-width: 1px;
  border-color: #4a5568;
  border-radius: 4px;
  font-family: inherit;
  padding: 1rem;
  padding-right: 1.5rem;
  padding-left: 1.5rem;
}
button {
  cursor: pointer;
  margin: 0.25rem;
  padding: 0.5rem;
  padding-right: 1.5rem;
  padding-left: 1.5rem;
  background-color: #2d3748;
  color: #edf2f7;
  border: solid;
  border-width: 1px;
  border-color: #4a5568;
  border-radius: 4px;
  font-family: inherit;
  font-size: 1.25rem;
  letter-spacing: 0.025em;
  font-weight: 300;
}
button:hover {
  background-color: #4a5568;
}
.hello {
  max-width: 640px;
  margin: auto;
  background-color: #1a202c;
}
</style>
