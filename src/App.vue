<template>
  <div>
      <aaa class="header"></aaa>
      <main class="mainHeader">
        <main-header></main-header>
        <cards></cards>
      </main>
      <div class="footer">
        <main-footer></main-footer>
      </div>
  </div>
</template>

<script>
import Aaa from "./components/aaa";
import MainHeader from "./components/MainHeader";
import Cards from "./components/Cards";
import MainFooter from "./components/MainFooter";

export default {
  // eslint-disable-next-line vue/no-unused-components
  components: {MainFooter, Cards, MainHeader, Aaa}
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Calibri, sans-serif;
  color: #9e9ea7;
}
main.mainHeader {
  width: 100%;
  height: auto;
  padding: 32px 72px 0 72px;
}


</style>