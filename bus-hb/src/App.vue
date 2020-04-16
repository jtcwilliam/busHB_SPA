<template >
  <div id="app">
    <!-- cabecalho -->
    <div class="cabecalho">
       
        <div class="row">
          <div class="col-sm-7 tituloCabecalho">Hamburgada do Bem - Reserva de Poltrona</div>
          <div class="col-sm-5">
            <img src="./assets/logo.png" />
          </div>
        </div>
     
    </div>

    <!-- corpo -->
 
    <div class="container">
      <div class="row">
        <div class="col-sm  ">
          <table class="table">
            
            <tbody>

             

 
              <tr>
                <td>
               
                  <ul>
                    <li class="classListaLink" v-for="pje in poltronasJanelaEsquerda">
                      <a class="btn poltronaLINK">{{pje}}</a>
                    </li>
                  </ul>
                </td>


                <td>
               
                  <ul>
                    <li class="classListaLink" v-for="pCe in poltronasCorredorEsquerda">
                      <a class="btn poltronaLINK">{{pCe}}</a>
                    </li>
                  </ul>
                </td>

                <td>
               
                  <ul>
                    <li class="classListaLink" v-for="pCd in poltronasCorredorDireita">
                      <a class="btn poltronaLINK">{{pCd}}</a>
                    </li>
                  </ul>
                </td>

                <td>
                 
                  <ul>
                    <li class="classListaLink" v-for="pJd in poltronasJanelaDireita">
                      <a class="btn poltronaLINK">{{pJd}}</a>
                    </li>
                  </ul>
                </td>
              </tr>
            </tbody>
          </table>
        </div>
        <div class="col-sm ">
          ---
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      color: "black",
      poltronasJanelaEsquerda: [],
      poltronasCorredorEsquerda: [],

      poltronasJanelaDireita: [],
      poltronasCorredorDireita: []
    };
  },

  created() {
    //janela esquerda
    let NumeroPoltronaJanelaEsquerda = 1;

    //corredor esquerdo
    let NumeroPoltronaCorredorEsquerda = 2;

    //corredor direita
    let NumeroPoltronaJanelaDireita = 3;

    //corredor direita
    let NumeroPoltronaCorredorDireita = 4;

    let contadorIA = 1;
    let contadorIB = 1;

    //trecho para montar as poltronas da esquerda(superior)
    while (contadorIA <= 11) {
      this.poltronasJanelaEsquerda.push(NumeroPoltronaJanelaEsquerda);
      this.poltronasCorredorEsquerda.push(NumeroPoltronaCorredorEsquerda);

      //janela esquerda
      NumeroPoltronaJanelaEsquerda += 4;

      //corredor esquerdo
      NumeroPoltronaCorredorEsquerda += 4;

      contadorIA++;
      // console.log(NumeroPoltronaJanelaA);
    }

    while (contadorIB <= 10) {
      this.poltronasJanelaDireita.push(NumeroPoltronaJanelaDireita);
      this.poltronasCorredorDireita.push(NumeroPoltronaCorredorDireita);

      if (contadorIB == 1) {
        this.poltronasJanelaDireita.push(" -");
        this.poltronasCorredorDireita.push(" - ");
        NumeroPoltronaJanelaDireita += 4;

        //corredor esquerdo
        NumeroPoltronaCorredorDireita += 4;
      } else {
        //janela esquerda
        NumeroPoltronaJanelaDireita += 4;

        //corredor esquerdo
        NumeroPoltronaCorredorDireita += 4;
      }

      contadorIB++;
      // console.log(NumeroPoltronaJanelaA);
    }

    this.poltronasJanelaEsquerda.push("43");
    this.poltronasCorredorEsquerda.push("44");
  }
};
</script>
 

<style>
html,
body {
  height: 100%;
  margin: 0;
  padding: 0;
}

@font-face {
  font-family: rogerserifBold;
  src: url("assets/fonts/roger-serif_bold-webfont.woff");
}

.classListaLink{
  list-style-type: none;
    color: white;
    padding-left: 0;
}
  
.btn {
  margin-top: 2vh;
  margin-left: 0px;
  color: aliceblue;
  background-color: navy;
  width: 10vh;
}

.tituloCabecalho {
  padding-top: 5vh;
  font-family: "Roger-Serif";
  font-size: x-large;
  height: 15vh;
}

.cabecalho {
  background-color: white;
  color: #4f8db7;
}
 
</style>
