<template>
  <footer>
    <span>Desenvolvido por<strong><a href="http://pedroflp.me" target="_blank"> Pedro Felipe</a></strong></span>
    <span><strong>{{ year }}</strong> - Esse site não possui nenhum vínculo ou afiliação direta com a Universidade Federal do Rio Grande do Norte.</span>
  </footer>
</template>

<script>
  const date = new Date();
  const year = date.getFullYear();

export default {
  name: "Footer",
  data() {
    return {
      year: year,
    }
  } 
}
</script>

<style>

footer{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 1rem;
}

footer span {
  color: rgb(163, 163, 163);
}

footer :last-child {
  letter-spacing: 0px;
  margin-top: 10px;
}

footer :last-child strong {
  letter-spacing: 1px;
}

footer a {
  text-decoration: none;
  cursor: pointer;
}
</style>