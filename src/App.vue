<template>
  <div id="app">
    <Header />
    <Calculator />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header';
import Calculator from './components/Calculator';
import Footer from './components/Footer';

export default {
  name: 'App',
  components: {
    Header,
    Calculator, 
    Footer
  }
}
</script>

<style>

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Roobert-Regular";
}

h1, h2, span, p {
  letter-spacing: -1px;
}

body {
  background: #e8e8e8;
}

:root {
  --main: "#6100d0";
}

</style>
