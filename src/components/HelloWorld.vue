<template>
  <div class="hello">
    <input v-model="innerInfo"/>
    <button @click="onClick">
      {{ editable }}
    </button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: ['editable', 'info'],
  methods: {
    onClick: function() {
      this.$emit('update:info', this.innerInfo)
    }
  },
  data() {
    return {
      innerInfo: this.info
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
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
