<template>
  <BasicLayouts>
      <main>
          <section class="banner" >
            <img class="img_header" src="../assets/img/medioambiente.jpg" alt="">
            <div class="content">
              <h1>EcoTripulantes</h1>
              <p>Es una apuesta para ayudar al medio ambiente mediante una comunidad.</p>
            <a  href="/login">ver más</a>
            </div>
            

        </section>
        <section class="welcom ui container">
          <h2>EcoTripulantes</h2>
          <p >El objetivo de la plataforma es ser un aliado de todas aquellas personas  en las cuales 
                exista un interés de trabajar en la preservación del medio ambiente o del reciclaje.
          </p>
        </section>

        <section style="box-shadow: 0 1px 4px 0; ">
          <div class="ui ">
            <div class="copyright">
              <h2 style="margin-top: 30px;">Clasificación de residuos</h2>
            </div>
            
          </div>
        <div class="ui  divided segment center aligned  grid" style="margin-top: 40px;">
          
          <div class="four wide center aligned column">
            <div class="ui card ali" style="background-color: #0c9154;">
              <div class="content center">
                <div class="header">ORDINARIOS</div>
              </div>
              <div class="content imge">
                <div class="ui small feed">
                  <div class="event">
                    <div class="content">
                      <div class="summary">
                        <div style="text-align: center">
                          <img class="recycle" src="../assets/img/Logo-Reciclado-white.png" alt="Logo reciclaje">
                        <p >Servilletas, empaques de papel plastificado, barrido, icopor, envases tetrapack
                        </p>
                        </div>
                        
                        </div>
                    </div>
                  </div>
                  
                </div>
              </div>
              <div class="extra content">
                <button class="ui button">
                  <router-link to="/post"> 
                    Ver máss
                    </router-link>
                </button>
              </div>
            </div>
  
          </div>
          <div class="four wide center ali aligned column">
            <div class="ui card ali" style="background-color: #ccab4f" >
              <div class="content center">
                <div class="header">ÓRGANICOS</div>
              </div>
              <div class="content imge">
                <div class="ui small feed">
                  <div class="event">
                    <div class="content">
                      <div class="summary">
                        <div style="text-align: center">
                          <img class="recycle" src="../assets/img/Logo-Reciclado-white.png" alt="Logo reciclaje">
                          <p >Residuos de alimentos, cáscaras de huevo, de frutas y vegetales no contaminados.
                          </p>
                        </div>
                        </div>
                    </div>
                  </div>
                  
                </div>
              </div>
              <div class="extra content">
                <button class="ui button">Ver más</button>
              </div>
            </div>
          </div>
          <div class="four wide center ali aligned column">
            <div class="ui card ali" style="background-color: #cac2bc">
              <div class="content center">
                <div class="header">PAPEL Y CARTÓN </div>
              </div>
              <div class="content ">
                <div class="ui small feed">
                  <div class="event">
                    <div class="content">
                      <div class="summary">
                        <div style="text-align: center">
                          <img class="recycle" src="../assets/img/Logo-Reciclado-white.png" alt="Logo reciclaje">
                          <p >Papel archivo, periódico, plegadiza, cartón liso y corrugado limpios y secos.
                        </p>
                        </div>
                        
                    
                        </div>
                    </div>
                  </div>
                  
                </div>
              </div>
              <div class="extra content">
                <button class="ui button">Ver más</button>
              </div>
            </div>
          </div>
        </div>
        <div class="ui  divided segment center aligned  grid" >
          <div class="four wide center ali aligned column">
              <div class="ui card ali" style="background-color: #3955a6">
                <div class="content center">
                  <div class="header">PLÁSTICOS</div>
                </div>
                <div class="content imge">
                  <div class="ui small feed">
                    <div class="event">
                      <div class="content">
                        <div class="summary">
                          <div style="text-align: center">
                            <img class="recycle" src="../assets/img/Logo-Reciclado-white.png" alt="Logo reciclaje">
                            <p >Bolsas plásticas, vasos, desechables, PET y contenedores plásticos limpios.
                            </p>
                          </div>
                          </div>
                      </div>
                    </div>
                    
                  </div>
                </div>
                <div class="extra content">
                  <button class="ui button">Ver más</button>
                </div>
              </div>
            </div>
            <div class="four wide center ali aligned column">
              <div class="ui card ali">
                <div class="content center">
                  <div class="header">VIDRIOS</div>
                </div>
                <div class="content imge">
                  <div class="ui small feed">
                    <div class="event">
                      <div class="content">
                        <div class="summary">
                          <div style="text-align: center">
                            <img class="recycle" src="../assets/img/Logo-Reciclado-white.png" alt="">
                            <p >Botellas, garrafas y contenedores de vidrios limpios.
                            </p>
                          </div>
                          </div>
                      </div>
                    </div>
                    
                  </div>
                </div>
                <div class="extra content">
                  <button class="ui button">Ver más</button>
                </div>
              </div>
            </div>
            <div class="four wide center  aligned column">
              <div class="ui card ali" style="background-color: #e82222">
                <div class="content center">
                  <div class="header">RESIDUOS PELIGROSOS</div>
                </div>
                <div class="content imge">
                  <div class="ui small feed">
                    <div class="event">
                      <div class="content">
                        <div class="summary">
                          <div style="text-align: center">
                            <img class="recycle" src="../assets/img/Logo-Reciclado-white.png" alt="">
                            <p >Baterias, pilas, insecticidas, aceites, aerosoles o productos tecnológicos. Residuos hospitalarios infecciosos.
                            </p>
                          </div>
                          </div>
                      </div>
                    </div>
                    
                  </div>
                </div>
                <div class="extra content">
                  <button class="ui button">Ver más</button>
                </div>
              </div>
          </div>
        </div>
        </section>
        
      </main>
      
  </BasicLayouts>
</template>

<script>
import BasicLayouts from '../layouts/BasicLayouts.vue'
export default {
  name: 'Home',
  components: { 
    BasicLayouts, 
  },

}
</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=IM+Fell+English+SC&family=Open+Sans:wght@500;600&display=swap');

.body {
  font-family: 'Open Sans', sans-serif;
  width: 100%;
  

}
.ui.card.ali {
   box-shadow:  0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}
.img_header{
  box-shadow:  0 1px 4px 0;
  width: 100%;
  height: 50%;
}
.text {
  text-align: center;
  
  
}
section {
  width: 100%;
  margin-bottom: 25px;
}

.banner{
  text-align: center;
  position: relative;
}

.banner .content {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translateX(-50%) translateY(-50%);
  color: white;
}

.banner h2{
  font-size: 40px;
}

.banner p {
  font-size: 20px;
}

.banner a {
  width: 100px;
  color: #fff !important;
  text-decoration: none;
  padding: 7px;
  border: 3px solid #fff;
 
}

.banner a:hover {
  background: rgba(51, 51, 51, 0.5);
}

.welcom {
  text-align: center;
}
.welcom p {
  font-size: 20px;
}
.residuos {
  margin-left: 60px;
        margin-right: 60px;
        align-items: center
}
.recycle{
 height: 83px !important;
}

</style>