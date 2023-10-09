<template>
  <v-footer class="bg-grey-lighten-1">
    <v-row justify="center" no-gutters>
      <v-btn color="white" class="mx-2" rounded="xl" variant="text" @click="$emit('navigate', 'about')">About</v-btn>
      <v-btn color="white" class="mx-2" rounded="xl" variant="text" @click="$emit('navigate', 'works')">Works</v-btn>
      <v-btn color="white" class="mx-2" rounded="xl" variant="text" @click="$emit('navigate', 'skill')">Skill</v-btn>
      <v-btn color="white" class="mx-2" rounded="xl" variant="text" @click="$emit('navigate', 'contact')">Contact</v-btn>
      <v-col class="text-center mt-4" cols="12">
        {{ new Date().getFullYear() }} — <strong>Morise Kentaro</strong>
      </v-col>
    </v-row>
  </v-footer>
</template>

<script>
export default {
  methods: {
  }
}
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