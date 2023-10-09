<template>
  <v-row justify="center">
    <v-col
        cols="12"
        sm="10"
        md="9"
        lg="8"
    >
        <div class="pa-4">
          <v-chip-group
              selected-class="text-primary"
              column
          >
            <v-chip
                v-for="tag in tags"
                :key="tag"
            >
              <v-btn
                  class="mr-2"
                  color="blue"
                  :icon="tag.icon"
                  size="22"
              ></v-btn>
              {{ tag.title }}
            </v-chip>
          </v-chip-group>
        </div>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data: () => ({
    tags: [
      {
        icon: "mdi-language-php",
        title: "php",
      },
      {
        icon: "mdi-laravel",
        title: "Laravel",
      },
      {
        icon: "mdi-language-javascrip",
        title: "JavaScript",
      },
      {
        icon: "mdi-vuejs",
        title: "Vue.js",
      },
      {
        icon: "mdi-vuetify",
        title: "Vuetify",
      },
      {
        icon: "",
        title: "MySQL",
      },
      {
        icon: "",
        title: "Verilog",
      },
      {
        icon: "",
        title: "SystemVerilog",
      },
      {
        icon: "mdi-language-python",
        title: "Python",
      },
      {
        icon: "mdi-language-java",
        title: "Java",
      },
      {
        icon: "mdi-docker",
        title: "Docker",
      },
      {
        icon: "mdi-terraform",
        title: "Terraform",
      },
      {
        icon: "mdi-aws",
        title: "AWS",
      },
      {
        icon: "mdi-linux",
        title: "Linux",
      },
      {
        icon: "mdi-ubuntu",
        title: "ubuntu",
      },
      {
        icon: "",
        title: "fpga",
      },
    ],
  }),
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

.works-list {
  display: flex;
  flex-wrap: wrap;
  margin-bottom: -40px;
}

.works-item {
  width: 31.74603%;
  margin-right: 1.58730%;
  margin-bottom: 40px;
  color: #333;
}

.works-item:hover {
  opacity: .9;
}

.works-item:nth-of-type(3n) {
  margin-right: 0;
}

.works-img img {
  border: 1px solid #e6e6e6;
}

.works-name {
  font-size: 12px;
  font-weight: bold;
  margin-top: 8px;
}

.works-info {
  font-size: 10px;
  margin-top: 5px;
}
</style>