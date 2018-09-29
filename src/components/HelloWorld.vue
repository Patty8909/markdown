<template>
  <div class="container">
    <h1>{{user.name}}</h1>
    <a href="#" class="b-skill" v-for="(framework,index) in user.frameworks" :key="index">{{framework}}</a>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      user: {
        name: 'Esmeralda',
        frameworks: [ 'React', 'Angular', 'Vue.js', 'Metal.js'],
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  $color-primary: #42b983;

  .container {
    max-width: 1024px;
    margin: o auto;
  }
  .b-skill {
    border: 4px solid darken ($color-primary, 5%);
    background: $color-primary;
    margin-right: 5px;
    color: white;
    border-radius: 10px 0;
    padding: 5px 15px 6px 15px;
    text-decoration: none;
    text-transform: uppercase;
  }
</style>
