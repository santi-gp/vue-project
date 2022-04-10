<!-- v-fpr with v-if-->
<template>
  <h3>Consolas</h3>
  <ul>
    <li v-for="(item, n) in consoles" :key="n">
      <strong>{{ item.title }}</strong>
      <ol v-if="item.game.length>0">
          <li v-for="(gam,m) in item.game" :key="m">
              {{gam}}
          </li>
      </ol>
    </li>
  </ul>
</template>

<script>
export default {
  name: "Vfor",
  data() {
    return {
      consoles: [
        {
          title: "Xbox",
          game: ["Fornite", 'Hallo']
        },
        {
          title: "PlayStation",
          game: ["Fifa",]
        },
        {
          title: "Nintendo",
          game: ["Mario Bross",'Zelda']
        },
      ],
    };
  },
};
</script>
<style scoped>
ol li{
    list-style-type:decimal;
    margin-left: 4%;
}
</style>

<!--<template>
<h3>Consolas</h3>
  <ul>
    <li v-for="(item, n) in consoles" :key="n">
      {{ item }}
    </li>
  </ul>
</template>
<script>
export default {
  name: "Vfor",
  data() {
    return {
      consoles: ["Xbox", "PlayStation", "Nintendo"],
    };
  },
};
</script>-->