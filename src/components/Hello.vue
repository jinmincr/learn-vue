<template>
  <div>
    <ul>
      <template v-for="item in items">
        <li>{{ item.message }}</li>
        <li class="divider"></li>
      </template>
    </ul>
    <span v-for="n in 10">{{ n }} </span>

    <div>
      <input type="checkbox" id="jack" value="Jack" v-model="checkedNames">
      <label for="jack">Jack</label>
      <input type="checkbox" id="john" value="John" v-model="checkedNames">
      <label for="john">John</label>
      <input type="checkbox" id="mike" value="Mike" v-model="checkedNames">
      <label for="mike">Mike</label>
      <br>
      <span>Checked names: {{ checkedNames }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data() {
    return {
      checkedNames: [],
      items: [
        { message: 'Foo' },
        { message: 'Bar' }
      ]
    };
  }
};
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
