<template>
  <div class="showBurger" @click="isOpen = !isOpen">
    <div class="burger1" v-if="!isOpen">
      <div></div>
      <div></div>
      <div></div>
    </div>
    <div class="burger" v-else>
      <div></div>
      <div></div>
      <div></div>
    </div>
  </div>
  <nav :class="isOpen ? 'closeNav' : 'nav'">
    <ul>
      <li><router-link to="/">Inicio</router-link></li>
      <li><router-link to="/about">About</router-link></li>
      <li><router-link to="/contact">Contact</router-link></li>
    </ul>
  </nav>
</template>
<script>
export default {
  name: "Burger",
  data() {
    return {
      isOpen: false,
    };
  },
};
</script>
<style scoped>
@media only screen and (min-width: 320px) and (max-width: 768px) {
  nav {
    position: fixed;
    top: 0;
    left: -100%;
    width: 66.67%;
    transition: all 0.5s ease;
  }
  ul {
    flex-direction: column;
    background-color: #00c7f1;
  }
  ul li{
    margin: 2% 0;
  }
  ul a {
    color: #1d213a;
  }
  .closeNav {
    left: 0;
  }
  .showBurger {
    width: 35px;
    height: max-content;
    cursor: pointer;
  }
  .burger1 div {
    background-color: #00c7f1;
    width: 35px;
    height: 5px;
    margin: 5px 0;
    transition: all 0.5s ease;
  }
  .burger div {
    background-color: #00c7f1;
    width: 35px;
    height: 5px;
    margin: 5px 0;
    transition: all 0.5s ease;
  }

  .burger div:nth-child(1) {
    transform: translate(0, 5px) rotate(45deg);
  }

  .burger div:nth-child(2) {
    display: none;
  }

  .burger div:nth-child(3) {
    transform: translate(0, -5px) rotate(-45deg);
  }
}
</style>
