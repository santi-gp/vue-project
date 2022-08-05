<template>
  <div>
    <div class="flex-row ai-center jc-around my-1">
      <button class="bgc-3 border-r5 pyx-1-2" @click="getFetchApi">Mostrar Fetch</button>
      <h3 class="color-1">Rick and Morty</h3>
      <button class="bgc-3 border-r5 pyx-1-2" @click="getAxiosApi">Mostrar Axios</button>
    </div>
    <ul>
      <li v-for="(item, n) in personages" :key="n">
        <img :src="item.image" alt="{item.name}" />
        <p class="my-2 color-1">{{ item.name }}</p>
      </li>
    </ul>
  </div>
</template>
<script>
import axios from "axios";
export default {
  name: "Fetch",
  data() {
    return {
      url: "https://rickandmortyapi.com/api/character/?page=1",
      personages: {},
    };
  },
  methods: {
    getFetchApi() {
      fetch(this.url)
        .then((response) => response.json())
        .then((mortys) => (this.personages = mortys.results));
    },
    async getAxiosApi() {
      return axios
        .get(this.url)
        .then((response) => (this.personages = response.data.results));
    },
  },
};
</script>
<style scoped>
ul {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
}
li {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: "2% 0";
}
img {
  width: 60%;
}
</style>