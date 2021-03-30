<template>
  <div class="header-container">
    <div class="header-title">
      <h1>UFRNCalc</h1>
      <p>Calcule sua média rápido e fácil, sem complicações e dúvidas.</p>
    </div>
    <img src="../assets/header-image.png">
  </div>
</template>

<script>

export default{

}
</script>

<style scoped>

.header-container {
  position: relative;
  display: flex;
  justify-content: center;
  background-size: cover;
  /*background: var(--main);*/
  background: linear-gradient(120deg,#7d41df 60%, #5a2ba5);

  padding: 1rem 5rem;
}

.header-title {
  max-width: 30rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-content: center;

  color: white;
}

.header-title h1 {
  font-size: 5rem;
  margin-bottom: 1rem;
  color: #00ff88;
  border-left: 3px solid #9756ff;
  padding-left: 1rem;
}

.header-title p {
  font-size: 1.5rem;
}

.header-container img {
  width: 25rem;
}

</style>