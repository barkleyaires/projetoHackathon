<template>
  <v-app class="body">
    <v-app-bar app color="#546224" dark>
      <div class="d-flex align-center">
        LOGO
      </div>

      <v-spacer></v-spacer>


        <span class="mr-2">Institucional |</span>
        


        <span class="mr-2"> Mapas | </span>
        <span class="mr-2"> Contatos </span>
    </v-app-bar>
    <v-spacer></v-spacer>
    <div class="thumbnail-wrapper">
      <v-carousel cycle interval="4000" height="550" hide-delimiter-background hide-delimiters>

        <v-carousel-item v-for="(item, i) in items" :key="i" :src="item.src"></v-carousel-item>
      </v-carousel>
      <h2 class="titles display-1 font-weight-bold mb-3">COMUNIDADES TRADICIONAIS</h2>
      <h1 class="sub display-1 mb-3">Mapas intuitivos</h1>
      <button class="teste"><a href="#conteudo5">Ver mais</a></button>
    </div>

    
      <section id="conteudo5">
        <l-map style="height: 600px" :zoom="zoom" :center="center">
          <l-tile-layer :url="url" :attribution="attribution"></l-tile-layer>
          <l-marker :lat-lng="markerLatLng">
            <l-popup>
              <h3>Quilombo Mumbuca </h3><br> Mumbuca é um povoado do município de Mateiros, que fica distante cerca de 360
              km da capital Palmas.

              O começo da história é lá nos anos 70, quando duas jovens mulheres da Bahia deixaram seu Estado de origem
              por sofrerem opressão por questões de trabalho e família.

              Na tentativa de se esconder de possíveis perseguidores, elas foram para o norte de Goiás (área que hoje
              pertence ao Tocantins) e se fixaram em vilarejos remotos, onde poucas pessoas circulavam por suas estradas
              de terra difíceis de chegar.
              <br>
              <v-btn color="primary" flat @click="dialog = false">
                <a href="#conteudo1">
                  Saiba Mais
                </a>
              </v-btn>
            </l-popup>
          </l-marker>
          <l-marker :lat-lng="markerLatLng2"></l-marker>
          <l-marker :lat-lng="markerLatLng3"></l-marker>
          <l-marker :lat-lng="markerLatLng4"></l-marker>
          <l-marker :lat-lng="markerLatLng5"></l-marker>
          <l-marker :lat-lng="markerLatLng6"></l-marker>
          <l-marker :lat-lng="markerLatLng7"></l-marker>
        </l-map>
      </section>



      <v-main>
      <section id="conteudo1">
        <HelloWorld />
      </section>
    </v-main>

  </v-app>
</template>
<link rel="stylesheet" href="//unpkg.com/leaflet/dist/leaflet.css" />
<script src="//unpkg.com/leaflet/dist/leaflet.js"></script>
<script src="//unpkg.com/vue2-leaflet"></script>
<script>
import HelloWorld from './components/HelloWorld';
import { LMap, LTileLayer, LMarker, LPopup } from 'vue2-leaflet';
import 'leaflet/dist/leaflet.css';

export default {
  name: 'App',

  components: {
    HelloWorld,
    LMap,
    LTileLayer,
    LMarker,
    LPopup
  },

  data: () => ({
    items: [
      {src: "https://uploaddeimagens.com.br/images/004/641/635/original/image1.jpeg?1697759905" },
      //{src: "https://static.wixstatic.com/media/480088_7bfebee6c018434887bed05830cef04b~mv2.jpg/v1/fill/w_640,h_360,al_c,q_80,usm_0.66_1.00_0.01,enc_auto/480088_7bfebee6c018434887bed05830cef04b~mv2.jpg" }
    ],
    url: 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png',
    attribution: '&copy; <a target="_blank" href="http://osm.org/copyright">OpenStreetMap</a> contributors',
    zoom: 6,
    center: [-8.551675110235465, -47.51278883247553],
    markerLatLng: [-10.548703, -46.416761],
    markerLatLng2: [-5.274499, -48.571623],
    markerLatLng3: [-11.618525, -47.752251],
    markerLatLng4: [-12.932377, -46.942507],
    markerLatLng5: [-9.755258, -48.358433],
    markerLatLng6: [-5.649914, -48.117853],
    markerLatLng7: [-8.054743, -48.485816

],
 
  }),
  methods: {
      redirect(){
        window.location.href = "http://www.devmedia.com.br";
      }
    }
};
</script>
<style>
.bt {
  height: 100px;
}

.thumbnail-wrapper {
  display: inline-block;
  position: relative;
}

.thumbnail-wrapper button {
  position: absolute;
  top: 70%;
  left: 50%;
  -webkit-transform: translate3d(-50%, -50%, 0);
  -moz-transform: translate3d(-50%, -50%, 0);
  transform: translate3d(-50%, -50%, 0);
}

.teste {
  background-color: #ffffff;
  /* Green */
  border: none;
  color: rgb(2, 2, 2);
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  border-radius: 12px;
  width: 300px;
  height: 50px;
}

.teste:hover {
  box-shadow: 0 12px 16px 0 rgba(0, 0, 0, 0.24), 0 17px 50px 0 rgba(0, 0, 0, 0.19);
}

.titles {
  position: absolute;
  top: 50%;
  left: 50%;
  -webkit-transform: translate3d(-50%, -50%, 0);
  -moz-transform: translate3d(-50%, -50%, 0);
  transform: translate3d(-50%, -50%, 0);
  color: #FFF;
  text-align: center;
  font-family: Inter;

  font-style: normal;

  line-height: normal;
}

.sub {
  position: absolute;
  top: 60%;
  left: 50%;
  -webkit-transform: translate3d(-50%, -50%, 0);
  -moz-transform: translate3d(-50%, -50%, 0);
  transform: translate3d(-50%, -50%, 0);
  color: #FFF;

  text-align: center;
  font-family: Inter;
  font-size: 25px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
}

.body {
  background-color: "#F5F5F5";
}

a {
  color: inherit !important;
  text-decoration: none !important;
}
</style>
