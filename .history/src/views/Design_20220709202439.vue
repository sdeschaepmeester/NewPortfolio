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
                  <h3 class="title">Section Design</h3>
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
                  background: linear-gradient(0deg, rgba(244,225,248,0.5747432762167367) 0%, rgba(226,201,237,0.3030345927433473) 100%); 
                  box-shadow: 1px 1px 10px 1px #6C5C78;
                  ">
                  <div class="md-layout-item ml-auto" style="margin: 15px">
                    <md-button @click="showModal(tabDrawings[0])"><img :src="tabDrawings[0].image" class="rounded" /></md-button>
                    <img :src="tabDrawings[1].image" class="rounded" />
                    <img :src="tabDrawings[2].image" class="rounded" />
                    <img :src="tabDrawings[3].image" class="rounded" />
                  </div>
                  <div class="md-layout-item ml-auto" style="margin: 15px">
                    <img :src="tabDrawings[4].image" class="rounded" />
                    <img :src="tabDrawings[5].image" class="rounded" />
                    <img :src="tabDrawings[6].image" class="rounded" />
                    <img :src="tabDrawings[7].image" class="rounded" />
                  </div>
                  <div class="md-layout-item ml-auto" style="margin: 15px">
                    <img :src="tabDrawings[8].image" class="rounded" />
                    <img :src="tabDrawings[9].image" class="rounded" />
                    <img :src="tabDrawings[11].image" class="rounded" />
                    <img :src="tabDrawings[12].image" class="rounded" />
                  </div>
                </div>
              </template>
              <template slot="tab-pane-2">
                <div class="md-layout" style="width: 90%; margin: auto; 
                  background: linear-gradient(0deg, rgba(244,225,248,0.5747432762167367) 0%, rgba(226,201,237,0.3030345927433473) 100%); 
                  box-shadow: 1px 1px 10px 1px #6C5C78;
                  ">
                  <div class="md-layout-item ml-auto" style="margin: 15px">
                    <img :src="tabAnimations[3].image" class="rounded" />
                    <img :src="tabAnimations[4].image" class="rounded" />
                  </div>
                  <div class="md-layout-item ml-auto" style="margin: 15px">
                    <img :src="tabAnimations[0].image" class="rounded" />
                    <img :src="tabAnimations[1].image" class="rounded" />
                  </div>
                  <div class="md-layout-item ml-auto" style="margin: 15px">
                    <img :src="tabAnimations[2].image" class="rounded" />
                  </div>
                </div>
              </template>
            </tabs>

              <modal v-if="modalShowImage" @close="modalShowImageHide">
                <template slot="header">
                  <h4 class="modal-title">Modal Title</h4>
                  <md-button
                    class="md-simple md-just-icon md-round modal-default-button"
                    @click="modalShowImageHide"
                  >
                    <md-icon>clear</md-icon>
                  </md-button>
                </template>
                <template slot="body">
                  <p>
                    Far far away, behind the word mountains, far from the
                    countries Vokalia and Consonantia, there live the blind
                    texts. Separated they live in Bookmarksgrove right at the
                    coast of the Semantics, a large language ocean. A small
                    river named Duden flows by their place and supplies it with
                    the necessary regelialia. It is a paradisematic country, in
                    which roasted parts of sentences fly into your mouth. Even
                    the all-powerful Pointing has no control about the blind
                    texts it is an almost unorthographic life One day however a
                    small line of blind text by the name of Lorem Ipsum decided
                    to leave for the far World of Grammar.
                  </p>
                </template>
                <template slot="footer">
                  <md-button
                    class="md-danger md-simple"
                    @click="modalShowImageHide"
                    >Close</md-button>
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
      ],
      tabAnimations: [
        { image: require("@/assets/img/animation/dog_computer.gif") },
        { image: require("@/assets/img/animation/fox_painting.gif") },
        { image: require("@/assets/img/animation/fox_first_anim.gif") },
        { image: require("@/assets/img/animation/fox_shelf.gif") },
        { image: require("@/assets/img/animation/fox_munching.gif") },
      ],
    };
  },
  props: {
    header: {
      type: String,
      default: require("@/assets/img/bg.png")
    },
    img: {
      type: String,
      default: require("@/assets/img/faces/christian.jpg")
    }
  },
  computed: {
    headerStyle() {
      return {
        backgroundImage: `url(${this.header})`
      };
    }
  },
  methods: {

    getRandomImg: function () {
      let random = Math.floor(Math.random() * this.tabDrawings.length);
      return this.tabDrawings[random].image
    },
    modalShowImageHide() {
      this.modalShowImage = false;
    },
    showModal(image){
      this.modalShowImage = true;
    }
  }
};
</script>

<style lang="scss" scoped>
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
