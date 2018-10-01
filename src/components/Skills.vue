<template>
  <div class="hello">
    <div class="holder">
      <ul>
        <li v-for="(data, index) in skills" :key='index'>{{index}}. {{data.skill}}</li>
      </ul>
    </div>
    <p v-if="skills.length >= 3">You have more than 2 skill</p>
    <p v-else>You have less than or equal to 2 skill</p>
  </div>
</template>

<script>
export default {
  name: 'Skills',
  data() {
    return {
      skills: [
          { "skill": "Vue.js" },
          { "skill": "Frontend Developer" }
      ]
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
