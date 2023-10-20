

<template>
  <v-container>

    <v-row class="text-center">
      <v-col cols="12">



      </v-col>


      <v-col class="mb-4 text1">
        <section id="conteudo3">
          <v-card class="mx-auto">
            <v-card-text class="pb-0">
              <p class="text-h4 text--primary">
                Quilombo Mumbuca
              </p>
              <p>Você sabia que a comunidade responsável pela produção de artesanato em capim dourado chama-se Mumbuca? Se
                não
                sabia, acompanhe esse texto para conhecer sua história!

                MUMBUCA: a comunidade do capim dourado

                A história do surgimento de Mumbuca é curiosa.

                Mumbuca é um povoado do município de Mateiros, que fica distante cerca de 360 km da capital Palmas.

                O começo da história é lá nos anos 70, quando duas jovens mulheres da Bahia deixaram seu Estado de origem
                por
                sofrerem opressão por questões de trabalho e família.

                Na tentativa de se esconder de possíveis perseguidores, elas foram para o norte de Goiás (área que hoje
                pertence ao Tocantins) e se fixaram em vilarejos remotos, onde poucas pessoas circulavam por suas estradas
                de
                terra difíceis de chegar.

                Com grande necessidade de sobrevivência e muita criatividade, viram nos fios de um capim bonito, que
                brilhava
                como ouro e era encontrado nas veredas, uma forma de ganhar o seu sustento. E assim começaram a
                confeccionar
                artesanatos a partir do capim dourado.

                Hoje a comunidade Mumbuca, que ganhou esse nome devido a um tipo de abelha da região, conta com
                aproximadamente 200 habitantes e produz com exclusividade o artesanato de capim dourado, admirado e
                exportado
                para todo o mundo!

                O CAPIM DOURADO

                O capim, que não é um capim, é, na verdade, um tipo de sempre-viva pertencente a família das
                Eriocaulaceas,
                cresce bem próximo ao solo em formato de roseta e acaba sendo escondido por outras plantas. Por isso,
                muitos
                comentam que colher o capim é quase que garimpar um ouro vegetal.

                As peças criadas vão desde bolsas, cestos, cintos, bijuterias, entre outras belíssimas obras de arte!

                Quer conhecer mais sobre o capim dourado e toda movimentação que ele traz na comunidade ano após ano?
                Então
                recomendamos assistir o documentário "Filhas do Dourado: Artesãs do Jalapão" clicando aqui.
              </p>
              <br><br>
            </v-card-text>
            <v-spacer></v-spacer>
          </v-card>

        </section>
      </v-col>
      <v-card class="mx-auto" max-width="344">
        <v-img src="https://alavoura.com.br/wp-content/uploads/2020/04/232602_1000-e1587579319434.jpg"
          height="200px"></v-img>

        <v-card-title>
          Capim Dourado
        </v-card-title>



        <v-btn color="orange lighten-2" text>
          Explore
        </v-btn>

        <v-spacer></v-spacer>




        <v-card-text>
          O capim, que não é um capim, é, na verdade, um tipo de sempre-viva pertencente a família das Eriocaulaceas,
          cresce bem próximo ao solo em formato de roseta e acaba sendo escondido por outras plantas. Por isso, muitos
          comentam que colher o capim é quase que garimpar um ouro vegetal.
        </v-card-text>

      </v-card>



    </v-row>
  </v-container>
</template>
<link rel="stylesheet" href="//unpkg.com/leaflet/dist/leaflet.css" />
<script src="//unpkg.com/leaflet/dist/leaflet.js"></script>
<script src="//unpkg.com/vue2-leaflet"></script>
<script>
  export default {
    name: 'HelloWorld',

    data () {
      return {
        dialog: false
      }
    },
    methods: {
      redirect(){
        window.location.href = "http://www.devmedia.com.br";
      }
    }
  }
</script>
<style>
.text1 {
  background-color: #FFF !important;
}
</style>

