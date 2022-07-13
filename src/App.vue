<template>
  <HeaderView />
  <MainView />
  <FooterView />
</template>

<script>
import FooterView from "./components/FooterView.vue";
import HeaderView from "./components/HeaderView.vue";
import MainView from "./components/MainView.vue";
export default {
  components: {
    HeaderView,
    MainView,
    FooterView,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
body {
  margin: 0;
}
#app {
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  margin: 0 auto;
  width: 100%;
  min-height: 100vh;
}
.margin-wrap {
	margin: 0 5%;
}
li {
  flex: 1;
  list-style-type: none;
}
a {
  display: block;
  text-decoration: none;
}
header,
footer {
  flex-shrink: 0;
  background-color: #1d213a;
}
header a {
  font-weight: bold;
  color: #fff;
}
main {
  /*display: flex;*/
  flex: 1 1 auto;
  /*background-color: #c0d7e4;*/
}
.main_content {
	display: flex;
	margin: 0 5%;
}
section {
  width: 70%;
  margin-top: 2%;
  
}
article {
  margin: 2% 1% 2% 2%;
}
aside {
  margin-top: 2%;
  width: 30%;
}
aside > div {
  margin: 2% auto;
  text-align: center;
}
footer p {
  margin: 1% 0;
  text-align: center;
  color: #fff;
}
header > div{
  padding: 2% 0;
  display: flex;
  justify-content: center;
  align-items: center;
}
header .logo {
  flex: 1;
  color: #00c7f1;
  
}
header nav {
  flex: 3;
}
nav ul {
  display: flex;
  flex: 1;
  justify-content: space-between;
  align-items: center;
  list-style: none;
}
nav a.router-link-exact-active {
  color: #42b983;
}

@media only screen and (min-width: 320px) and (max-width: 768px) {
  .wrapper {
    width: 100%;
  }
  .margin-wrap, .main_content{
    margin: 0 2%;
  }
  .main_content{
    flex-direction: column;
  }
  header,
  section,
  aside {
    width: 100%;
  }
  main {
    flex-direction: column;
  }
  
  
}
</style>
