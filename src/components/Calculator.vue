<template>
  <div class="calculator-container">
    <div class="calculator-input">
      <input type="number" min="0" step="any" max="10" minlength="1" maxlength="4" >
      <input type="number" min="0" step="any" max="10" minlength="1" maxlength="4" >
      <input type="number" min="0" step="any" max="10" minlength="1" maxlength="4" > 
    </div>
    <button>Calcular média</button>
  </div>
</template>

<script>
export default {
  name: "Calculator",
}

</script>

<style scoped>

.calculator-container {
  display: flex;
  justify-content: center;
  align-content: center;

  width: 35rem;
  
  padding: 2rem;
  margin: auto;

  position: relative;
}

.calculator-input {
  position: absolute;
  top: 0;
  margin-top: -45px;
  margin-bottom: 40px;
}

.calculator-input input {
  width: 10rem;
  padding: 1.5rem;
  margin: 0 5px;
  border-radius: 5px;
  border: 2px solid transparent;
  color: #5400bb;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  font-size: 2rem;
  letter-spacing: 2px;
  font-weight: 900;
  text-align: center;
  outline: none;
  transition: 0.4s ease-in-out;
}

.calculator-input input:focus {
  border-color: #5400bb;
}

.calculator-container button {
  flex: 1;
  margin-top: 40px;
  height: 4rem;
  color: white;
  background: #7732f7;
  font-weight: 600;
  letter-spacing: 1px;
  font-size: 1.1rem;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  outline: none;
  transition: 0.3s ease-in-out;
}

.calculator-container button:hover {
  transform: translateY(-5px);
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}

</style>