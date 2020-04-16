    <template >
      <div id="app" >
          <div class="cabecalho">
              <div class="container"> 
                <div class="row">
                  <div class="col-sm-7   tituloCabecalho">
                      Hamburgada do Bem - Reserva de Poltrona
                  </div>
                  
                  <div class="col-sm-5   ">
                    <img src="./assets/logo.png" />
                  </div>
                </div>
              </div>

          </div>
      </div>
    
    
    </template>

    <script>
    export default {
      name: 'App',

      data() {
        return {
          color: 'black'
        }
      }
    }
    </script>

    <style>

    html, body {
      height: 100%;
      margin: 0;
      padding: 0;
    }

      @font-face { font-family: Roger-Serif; src:url('assets/fonts/roger-serif_bold-webfont.woff'); }


    .tituloCabecalho{
      padding-top: 5vh;
      font-family: 'Roger-Serif';
      font-size: x-large;
      height: 10vh;
    }


    .cabecalho{

      background-color: white;
      color: #4F8DB7;
      
      ;

    }



    #app {
      /*
      font-family: 'Avenir', Helvetica, Arial, sans-serif;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
      text-align: center;
      color: whitesmoke;
      margin-top: 60px;
      */
    }
    </style>
