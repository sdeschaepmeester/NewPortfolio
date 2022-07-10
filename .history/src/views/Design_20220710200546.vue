<template>
  <div class="wrapper">
    <parallax
      class="section page-header"
      :style="headerStyle"
    ></parallax>
    <div class="main main-raised">
      <div class="section">
        <div class="container">
          <div class="md-layout">
            <div class="md-layout-item md-size-50 mx-auto">
              <div class="profile">
                <div class="avatar">
                </div>
                <div class="name">
                  <h3 class="title" style="color: white" >Design & Animations</h3>
                </div>
              </div>
            </div>
          </div>
          <div class="description text-center">
            <p>
              Ayant toujours eu un attrait pour les arts, j'ai pris l'initiative d'apprendre par moi-même le dessin sur tablette, pour par la suite apprendre à faire des animations 2D.
            </p>
          </div>

          <!-- <div class="md-layout-item md-size-50">
              <div style="height: 250px; width: 350px; backgroundColor: grey">
                <img :src="getRandomImg()" class="rounded" contain />
              </div>
            </div> -->

          <div class="profile-tabs">
 
            <tabs
              :tab-name="['Dessins', 'Animations']"
              :tab-icon="['palette', 'movie']"
              plain
              nav-pills-icons
              color-button="success"
            >
              <!-- here you can add your content for tab-content -->
              <template slot="tab-pane-1">
                <div class="md-layout" style="width: 90%; margin: auto; 
                  background: linear-gradient(0deg, rgba(233,237,233,0.08734831823354339) 0%, rgba(193,245,191,0.1461718476453081) 100%); 
                  box-shadow: 1px 1px 10px 1px #154d1a;
                  ">
                  <div class="md-layout-item ml-auto" style="margin: 15px">
                    <img @click="showModal(tabDrawings[0])" :src="tabDrawings[0].image" class="rounded" />
                    <img @click="showModal(tabDrawings[1])" :src="tabDrawings[1].image" class="rounded" />
                    <img @click="showModal(tabDrawings[2])" :src="tabDrawings[2].image" class="rounded" />
                    <img @click="showModal(tabDrawings[3])" :src="tabDrawings[3].image" class="rounded" />
                    <img @click="showModal(tabDrawings[13])" :src="tabDrawings[13].image" class="rounded" />
                  </div>
                  <div class="md-layout-item ml-auto" style="margin: 15px">
                    <img @click="showModal(tabDrawings[4])" :src="tabDrawings[4].image" class="rounded" />
                    <img @click="showModal(tabDrawings[5])" :src="tabDrawings[5].image" class="rounded" />
                    <img @click="showModal(tabDrawings[6])" :src="tabDrawings[6].image" class="rounded" />
                    <img @click="showModal(tabDrawings[7])" :src="tabDrawings[7].image" class="rounded" />
                    <img @click="showModal(tabDrawings[16])" :src="tabDrawings[16].image" class="rounded" />
                  </div> 
                  <div class="md-layout-item ml-auto" style="margin: 15px">
                    <img @click="showModal(tabDrawings[8])" :src="tabDrawings[8].image" class="rounded" />
                    <img @click="showModal(tabDrawings[9])" :src="tabDrawings[9].image" class="rounded" />
                    <img @click="showModal(tabDrawings[11])" :src="tabDrawings[11].image" class="rounded" />
                    <img @click="showModal(tabDrawings[12])" :src="tabDrawings[12].image" class="rounded" />
                    <img @click="showModal(tabDrawings[15])" :src="tabDrawings[15].image" class="rounded" />
                  </div>
                </div>
              </template>
              <template slot="tab-pane-2">
                <div class="md-layout" style="width: 90%; margin: auto; 
                  background: linear-gradient(0deg, rgba(233,237,233,0.08734831823354339) 0%, rgba(193,245,191,0.1461718476453081) 100%); 
                  box-shadow: 1px 1px 10px 1px #154d1a;
                  ">
                  <div class="md-layout-item ml-auto" style="margin: 15px">
                    <img @click="showModal(tabAnimations[3])" :src="tabAnimations[3].image" class="rounded" />
                    <img @click="showModal(tabAnimations[4])" :src="tabAnimations[4].image" class="rounded" />
                  </div>
                  <div class="md-layout-item ml-auto" style="margin: 15px">
                    <img @click="showModal(tabAnimations[0])" :src="tabAnimations[0].image" class="rounded" />
                    <img @click="showModal(tabAnimations[1])" :src="tabAnimations[1].image" class="rounded" />
                  </div>
                  <div class="md-layout-item ml-auto" style="margin: 15px">
                    <img @click="showModal(tabAnimations[2])" :src="tabAnimations[2].image" class="rounded" />
                  </div>
                </div>
              </template>
            </tabs>

              <modal v-if="modalShowImage" @close="modalShowImageHide" class="modalImage">
                <template slot="header">
                  <h4 class="modal-title">{{modalImage.name}}</h4>
                  <md-button class="md-simple md-just-icon md-round modal-default-button" @click="modalShowImageHide" > <md-icon>clear</md-icon> </md-button>
                </template>
                <template slot="body">
                  <img :src="modalImage.image" class="imageInModal"/>
                  <p>{{modalImage.description}}</p>
                </template>
              </modal>

            <p style="marginBottom: 20px"> 
              Un de mes objectifs étant de faire la promotion de mon jeu mobile sous forme de vidéo animée par des animation 2D, 
              beaucoup de ces dessins ont pour sujet un ou plusieurs personnages de mon jeu.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { Tabs } from "@/components";
import { Modal } from "@/components";
export default {
  components: {
    Tabs,
    Modal
  },
  bodyClass: "profile-page",
  data() {
    return {
      modalShowImage: false,
      modalImage: null,
      tabDrawings: [
        { image: require("@/assets/img/drawing/neon-fox.png"), name: "Neon fox", description: "Un entrainement pour apprendre à dessiner l'effet néon."},
        { image: require("@/assets/img/drawing/fox-pumpkin.png"), name: "Fox Pumpkin", description: "Dessin représentant le renard de mon jeu sur une citrouille." },
        { image: require("@/assets/img/drawing/andrew.png"), name: "Andrew", description: "Ma tourterelle, fidèle associé." },
        { image: require("@/assets/img/drawing/foxmoon.png"), name: "Fox under the moon", description: "Un entrainement pour apprendre à dessiner l'effet néon." },
        { image: require("@/assets/img/drawing/github.png"), name: "Me and my pets", description: "Ma bannière Github" },
        { image: require("@/assets/img/drawing/black-fox.png"), name: "Black fox", description: "Un personnage de mon jeu." },
        { image: require("@/assets/img/drawing/fox-silhouette1.png"), name: "Fox silhouette", description: "Silhouette de renard." },
        { image: require("@/assets/img/drawing/fox-silhouette2.png"), name: "Fox silhouette", description: "Silhouette de renard." },
        { image: require("@/assets/img/drawing/fox-sketch.png"), name: "Fox sketches", description: "Apprendre à dessiner les renards sous diverses positions." },
        { image: require("@/assets/img/drawing/knight_full.png"), name: "Artorias Knight", description: "Apprendre à dessiner un humain en suivant un modèle." },
        { image: require("@/assets/img/drawing/knight.png"), name: "Artorias Knight", description: "Apprendre à dessiner un humain en suivant un modèle." },
        { image: require("@/assets/img/drawing/logo.png"), name: "Andrew logo", description: "Un logo que j'utilise." },
        { image: require("@/assets/img/drawing/coyote.png"), name: "Coyote", description: "Un personnage de mon jeu." },
        { image: require("@/assets/img/drawing/lake.png"), name: "Pink lake", description: "Voyez la vie en rose !" },
        { image: require("@/assets/img/drawing/lakegreen.png"), name: "Green lake", description: "Un paysage de lac aux tons verts." },
        { image: require("@/assets/img/drawing/lakewithpin.png"), name: "Lake with fir", description: "Un paysage de lac, avec un sapin." },
        { image: require("@/assets/img/drawing/meadow.png"), name: "Meadow landscape", description: "Un paysage de prairie." },
        { image: require("@/assets/img/drawing/mill.png"), name: "Mill landscape", description: "Un paysage avec un moulin" },
        { image: require("@/assets/img/drawing/swan.png"), name: "Swan landscape", description: "Un paysage de lac avec un cygne." },
      ],
      tabAnimations: [
        { image: require("@/assets/img/animation/dog_computer.gif"), name: "Coding dog", description: "Un personnage de mon jeu." },
        { image: require("@/assets/img/animation/fox_painting.gif"), name: "Painting fox", description: "Le renard, héro de mon jeu." },
        { image: require("@/assets/img/animation/fox_first_anim.gif"), name: "My pet fox", description: "Psst ! Ce n'est pas le vrai nom du jeu." },
        { image: require("@/assets/img/animation/fox_shelf.gif"), name: "My pet fox", description: "Une animation faite pour illustrer mon premier article LinkedIn."},
        { image: require("@/assets/img/animation/fox_munching.gif"), name: "Fox munching bone", description: "Tentative de dessiner un renard sous un style différent, plus 'sketch'." },
      ],
    };
  },
  props: {
    header: {
      type: String,
      default: require("@/assets/img/swan.png")
    },
    img: {
      type: String,
      default: require("@/assets/img/faces/christian.jpg")
    }
  },
  computed: {
    headerStyle() {
      return {
        backgroundImage: `url(${this.header})`,
        resize: 'contain!important'
      };
    }
  },
  methods: {

    getRandomImg: function () {
      let random = Math.floor(Math.random() * this.tabDrawings.length);
      return this.tabDrawings[random].image
    },
    modalShowImageHide() {
      this.modalImage = null;
      this.modalShowImage = false;
    },
    showModal(image){
      this.modalImage = image;
      this.modalShowImage = true;
    }
  }
};
</script>

<style lang="scss" scoped>

.headerImg{
  resize: contain!important;
}

.imageInModal{
  max-height: 250px;
  max-width: 500px;
}

.modalImage {
  height: 500px!important;
  position: fixed!important;
  margin-top: 5%!important;
}

.section {
  padding: 0;
}

.profile-tabs::v-deep {
  .md-card-tabs .md-list {
    justify-content: center;
  }

  [class*="tab-pane-"] {
    margin-top: 3.213rem;
    padding-bottom: 50px;

    img {
      margin-bottom: 2.142rem;
    }
  }
}
</style>
