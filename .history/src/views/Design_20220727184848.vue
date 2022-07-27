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
                    <img @click="showModal(getObjById('neon-fox','drawing'))" :src="getImgById('neon-fox','drawing')" class="rounded imageSmall" />
                    <img @click="showModal(getObjById('andrew','drawing'))" :src="getImgById('andrew','drawing')" class="rounded imageSmall" />
                    <img @click="showModal(getObjById('knight-full','drawing'))" :src="getImgById('knight-full','drawing')" class="rounded imageSmall" />
                    <img @click="showModal(getObjById('meadow','drawing'))" :src="getImgById('meadow','drawing')" class="rounded imageSmall" />
                    <img @click="showModal(getObjById('fox-pumpkin','drawing'))" :src="getImgById('fox-pumpkin','drawing')" class="rounded imageSmall" />
                    <img @click="showModal(getObjById('fire','drawing'))" :src="getImgById('fire','drawing')" class="rounded imageSmall" />
                    <img @click="showModal(getObjById('ghost-fox','drawing'))" :src="getImgById('ghost-fox','drawing')" class="rounded imageSmall" />
                  </div>
                  <div class="md-layout-item ml-auto" style="margin: 15px">
                    <img @click="showModal(getObjById('me-and-pets','drawing'))" :src="getImgById('me-and-pets','drawing')" class="rounded imageSmall" />
                    <img @click="showModal(getObjById('black-fox','drawing'))" :src="getImgById('black-fox','drawing')" class="rounded imageSmall" />
                    <img @click="showModal(getObjById('fox-moon','drawing'))" :src="getImgById('fox-moon','drawing')" class="rounded imageSmall" />
                    <img @click="showModal(getObjById('fox-sunset','drawing'))" :src="getImgById('fox-sunset','drawing')" class="rounded imageSmall" />
                    <img @click="showModal(getObjById('mill','drawing'))" :src="getImgById('mill','drawing')" class="rounded imageSmall" />
                    <img @click="showModal(getObjById('isle','drawing'))" :src="getImgById('isle','drawing')" class="rounded imageSmall" />
                    <img @click="showModal(getObjById('fox-sketch','drawing'))" :src="getImgById('fox-sketch','drawing')" class="rounded imageSmall" />
                  </div> 
                  <div class="md-layout-item ml-auto" style="margin: 15px">
                    <img @click="showModal(getObjById('lake-tree','drawing'))" :src="getImgById('lake-tree','drawing')" class="rounded imageSmall" />
                    <img @click="showModal(getObjById('fox-bubbles','drawing'))" :src="getImgById('fox-bubbles','drawing')" class="rounded imageSmall" />
                    <img @click="showModal(getObjById('lake-green','drawing'))" :src="getImgById('lake-green','drawing')" class="rounded imageSmall" />
                    <img @click="showModal(getObjById('swan','drawing'))" :src="getImgById('swan','drawing')" class="rounded imageSmall" />
                    <img @click="showModal(getObjById('logo','drawing'))" :src="getImgById('logo','drawing')" class="rounded imageSmall" />
                    <img @click="showModal(getObjById('lake','drawing'))" :src="getImgById('lake','drawing')" class="rounded imageSmall" />
                    <img @click="showModal(getObjById('bubbles','drawing'))" :src="getImgById('bubbles','drawing')" class="rounded imageSmall" />
                  </div>
                </div>
              </template>
              <template slot="tab-pane-2">
                <div class="md-layout" style="width: 90%; margin: auto; 
                  background: linear-gradient(0deg, rgba(233,237,233,0.08734831823354339) 0%, rgba(193,245,191,0.1461718476453081) 100%); 
                  box-shadow: 1px 1px 10px 1px #154d1a;
                  ">
                  <div class="md-layout-item ml-auto" style="margin: 15px">
                    <img @click="showModal(getObjById('fox-shelf','animation'))" :src="getImgById('fox-shelf','animation')" class="rounded imageSmall" />
                    <img @click="showModal(getObjById('fox-munching','animation'))" :src="getImgById('fox-munching','animation')" class="rounded imageSmall" />
                  </div>
                  <div class="md-layout-item ml-auto" style="margin: 15px">
                    <img @click="showModal(getObjById('dog-computer','animation'))" :src="getImgById('dog-computer','animation')" class="rounded imageSmall" />
                    <img @click="showModal(getObjById('fox-painting','animation'))" :src="getImgById('fox-painting','animation')" class="rounded imageSmall" />
                  </div>
                  <div class="md-layout-item ml-auto" style="margin: 15px">
                    <img @click="showModal(getObjById('pet-fox','animation'))" :src="getImgById('pet-fox','animation')" class="rounded imageSmall" />
                  </div>
                </div>
              </template>
            </tabs>

              <modal v-if="modalShowImage" @close="modalShowImageHide" class="modal-lg">
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
              Un de mes objectifs étant de faire la promotion de mon jeu mobile sous forme de vidéo animée par des animations 2D, 
              beaucoup de ces dessins ont pour sujet un ou plusieurs personnages de mon jeu (des renards).
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
        { id: "neon-fox", image: require("@/assets/img/drawing/neon-fox.png"), name: "Neon fox", description: "Un entrainement pour apprendre à dessiner l'effet néon."},
        { id: "fox-pumpkin", image: require("@/assets/img/drawing/fox-pumpkin.png"), name: "Pumpkin fox", description: "Dessin représentant le renard de mon jeu sur une citrouille." },
        { id: "andrew", image: require("@/assets/img/drawing/andrew.png"), name: "Andrew", description: "Ma tourterelle, fidèle associé." },
        { id: "fox-moon", image: require("@/assets/img/drawing/foxmoon.png"), name: "Renard sous la lune", description: "Un entrainement pour apprendre à dessiner l'effet néon." },
        { id: "me-and-pets", image: require("@/assets/img/drawing/github.png"), name: "Moi et mes animaux", description: "Ma bannière Github" },
        { id: "black-fox", image: require("@/assets/img/drawing/vista-snow.png"), name: "Renard noir", description: "Un personnage de mon jeu." },
        { id: "fox-sunset", image: require("@/assets/img/drawing/fox-sunset.png"), name: "Renard avec coucher de soleil", description: "Un entrainement pour apprendre les dégradés." },
        { id: "fox-bubbles", image: require("@/assets/img/drawing/fox-bubbles.png"), name: "Fox silhouette", description: "Une silhouette que j'utilise dans des bannières." },
        { id: "fox-sketch", image: require("@/assets/img/drawing/fox-sketch.png"), name: "Fox sketches", description: "Apprendre à dessiner les renards sous diverses positions." },
        { id: "knight-full", image: require("@/assets/img/drawing/knight_full.png"), name: "Artorias Knight", description: "Apprendre à dessiner un humain en suivant un modèle (Hero forge)." },
        { id: "knight", image: require("@/assets/img/drawing/knight.png"), name: "Artorias Knight", description: "Apprendre à dessiner un humain en suivant un modèle (Hero forge)." },
        { id: "logo", image: require("@/assets/img/drawing/logo.png"), name: "Andrew logo", description: "Un logo que j'utilise représentant mon oiseau." },
        { id: "coyote", image: require("@/assets/img/drawing/coyote.png"), name: "Coyote", description: "Un personnage de mon jeu." },
        { id: "lake", image: require("@/assets/img/drawing/lake.png"), name: "Pink lake", description: "Voyez la vie en rose !" },
        { id: "lake-green", image: require("@/assets/img/drawing/lakegreen.png"), name: "Green lake", description: "Un paysage de lac aux tons verts." },
        { id: "lake-tree", image: require("@/assets/img/drawing/lakewithpin.png"), name: "Lake with fir", description: "Un paysage de lac, avec un sapin." },
        { id: "meadow", image: require("@/assets/img/drawing/meadow.png"), name: "Meadow landscape", description: "Un paysage de prairie." },
        { id: "mill", image: require("@/assets/img/drawing/mill.png"), name: "Mill landscape", description: "Un paysage avec un moulin" },
        { id: "swan", image: require("@/assets/img/drawing/swan.png"), name: "Swan landscape", description: "Un paysage de lac avec un cygne." },
        { id: "fire", image: require("@/assets/img/drawing/fire.png"), name: "Fire", description: "Premier tentative de dessiner du feu." },
        { id: "isle", image: require("@/assets/img/drawing/isle.png"), name: "Ile dans le ciel", description: "Sera repris comme modèle d'entrainement pour dessiner des nuages." },
        { id: "bubbles", image: require("@/assets/img/drawing/bubbles.png"), name: "Bubbles", description: "Des bubulles." },
        { id: "ghost-fox", image: require("@/assets/img/drawing/ghost-fox.png"), name: "Ghost fox", description: "SpOoky !" },
      ],
      tabAnimations: [
        { id: "dog-computer", image: require("@/assets/img/animation/dog_computer.gif"), name: "Coding dog", description: "Un personnage de mon jeu." },
        { id: "fox-painting", image: require("@/assets/img/animation/fox_painting.gif"), name: "Painting fox", description: "Le renard héro de mon jeu." },
        { id: "pet-fox", image: require("@/assets/img/animation/fox_first_anim.gif"), name: "My pet fox", description: "Psst ! Ce n'est pas le vrai nom du jeu." },
        { id: "fox-shelf", image: require("@/assets/img/animation/fox_shelf.gif"), name: "My pet fox", description: "Une animation faite pour illustrer mon premier article LinkedIn."},
        { id: "fox-munching", image: require("@/assets/img/animation/fox_munching.gif"), name: "Fox munching bone", description: "Tentative de dessiner un renard sous un style différent, plus 'sketch'." },
      ],
    };
  },
  props: {
    header: {
      type: String,
      default: require("@/assets/img/test.png")
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
    getObjById: function (id, imageType) {
      let imageFound;
      if(imageType === "drawing"){
        imageFound = this.tabDrawings.find((drawing) => drawing.id == id);
      }else{
        imageFound = this.tabAnimations.find((animation) => animation.id == id);
      }
      return imageFound;
    },
    getImgById: function (id, imageType) {
      let imageFound;
      if(imageType === "drawing"){
        imageFound = this.tabDrawings.find((drawing) => drawing.id == id);
      }else{
        imageFound = this.tabAnimations.find((animation) => animation.id == id);
      }
      return imageFound.image;
    },

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
modal{
  height: 800px!important;
}

.imageSmall:hover{
  cursor: zoom-in!important;
}

.imageInModal{
  max-height: 90%;
  max-width: 500px;
}

.modalImage {
  width: 100%!important;
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
