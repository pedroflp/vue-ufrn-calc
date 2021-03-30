<template>
  <div class="calculator-container">
    <div class="calculator-input">
      <input type="number" v-model="nota_1">
      <input type="number" v-model="nota_2">
      <input type="number" v-model="nota_3"> 
    </div>
    <button @click="calcularMedia()" >Calcular média</button>
  </div>
</template>

<script>
export default {
  name: "Calculator",
  data() {
    return {
      nota_1: Number,
      nota_2: Number,
      nota_3: Number,
    }
  },
  methods: {
    calcularMedia: function() {
      var nota_1 = parseFloat(this.nota_1);
      var nota_2 = parseFloat(this.nota_2);
      var nota_3 = parseFloat(this.nota_3);

      var nota_4 = parseFloat(0);
      var nota_parcial = parseFloat(0);
      var media = parseFloat(0);


      // NÃO CALCULAR n>10
      if (nota_1 > 10 || nota_2 > 10 || nota_3 > 10 || nota_1 < 0 || nota_2 < 0 || nota_3 < 0 || nota_1 == null || nota_2 == null || nota_3 == null) {
        return console.log('insira nota <= 10')
      }

      nota_parcial = (nota_1 + nota_2 + nota_3);
      console.log('Nota: ' + nota_parcial)
      media = (nota_parcial / 3).toFixed(2);
      console.log('Média: ' + media)


      if (media >= 3){
          if ((nota_1 == nota_2) && (nota_1 == nota_3)) {
            nota_4 = 15 - nota_2 - nota_3;
          } else {
            if ((nota_1 < nota_2) && (nota_1 < nota_3)) {
              nota_4 = 15 - nota_2 - nota_3;
            } else {
              if ((nota_2 < nota_1) && (nota_2 < nota_3)) {
                  nota_4 = 15 - nota_1 - nota_3;
              } else {
                  nota_4 = 15 - nota_1 - nota_2;
              }
            }
          }
          
          if (nota_4 < 3) {
            nota_4 = 3;
          }
      }
          
      // UMA NOTA ABAIXO DE 3
      if ((nota_1 < 3 && nota_2 >= 3 && nota_3 >= 3) || (nota_1 >= 3 && nota_2 < 3 && nota_3 >= 3) || (nota_1 >= 3 && nota_2 >= 3 && nota_3 < 3) || (nota_1 == 3 && nota_2 == 3 && nota_3 == 3) || (nota_1 >= 3 && nota_2 >= 3 && nota_3 >= 3 && nota_parcial >= 3 && nota_parcial < 5)) {
        // aprovado por média >= 7 com uma abaixo de 3
        if (media >= 7) {
          console.log('aprovado');
        } else { 
          // precisa fazer p4
          console.log('p4');
          console.log('precisa tirar: ' + nota_4)
        }

      } else {
          // reprovado
          if ((nota_1 < 3 && nota_2 < 3 && nota_3 < 3)){
            console.log('reprovado');

          } else {
            // reprovado por média < 7 e duas notas < 3
            if((nota_1 < 3 && nota_2 < 3) || (nota_1 < 3 && nota_3 < 3) || (nota_2 < 3 && nota_3 < 3 )) {
              console.log('reprovado por duas notas < 3 e media < 7')
            }
          } 

          // APROVADO
          if (media >= 5 && media < 7) {
            // aprovado por media >= 5 e < 7
            if (nota_1 >= 3 && nota_2 >= 3 && nota_3 >=3) { 
              console.log('aprovado por nota')
            }
          } else {
            // aprovado por media >= 7
            if (media >= 7) {
              console.log('aprovado')
            }
          }
      }
      
      }
    }
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