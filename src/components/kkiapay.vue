<template>
  <div class="hello">
    <ul>
      <a @click.prevent="openWidget">openKkiapayWidget</a>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  mounted() {},
  methods: {
    openWidget() {
      window.openKkiapayWidget({
        sandbox: true,
        amount: "3000",
        key: "xxxxxx"
      });
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
