<template>
  <v-carousel
      cycle
      height="400"
      hide-delimiter-background
      show-arrows="hover"
  >
    <v-carousel-item
        v-for="(slide, i) in slides"
        :key="i"
    >
      <v-sheet
          :style="`background-image: url('https://picsum.photos/1920/1080?random&seed=${i}'); background-size: cover; background-position: center;`"
          height="100%"
      >
        <div class="d-flex fill-height justify-center align-center">
          <div class="text-h2">
            MORISE KENTARO
          </div>
        </div>
      </v-sheet>
    </v-carousel-item>
  </v-carousel>
</template>

<script>
export default {
  data () {
    return {
      slides: [
        'First',
        'Second',
        'Third',
        'Fourth',
        'Fifth',
      ],
    }
  },
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