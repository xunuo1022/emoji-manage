<template>
  <div>
    <Header></Header>
    <Nav></Nav>
    <Main></Main>
    <Backtop></Backtop>
  </div>
</template>

<style>
* {
  margin: 0;
  padding: 0;
}
</style>

<style scoped>
div {
  background-color: #f5f5f5;
}
</style>

<script>
import Header from "@/components/header/header.vue";
import Nav from "@/components/nav/nav.vue";
import Main from "@/components/main/main.vue";
import Backtop from "@/components/backtop/backtop.vue";

export default {
  components: {
    Header,
    Nav,
    Main,
    Backtop,
  },
};
</script>
