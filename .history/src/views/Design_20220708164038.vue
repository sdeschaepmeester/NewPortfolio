<template>
  <div class="wrapper">
    <parallax
      class="section page-header header-filter"
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
                  <h3 class="title">Design</h3>
                </div>
              </div>
            </div>
          </div>
          <div class="description text-center">
            <p>
              Férue de dessin et de peinture, j'ai pris l'initiative d'apprendre par moi-même le dessin sur tablette, pour par la suite apprendre à faire des animations 2D.
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
                  background: linear-gradient(186deg, rgba(238,241,209,0.6139589624912465) 0%, rgba(237,212,201,0.7568161053483894) 100%);   ">
                  <div class="md-layout-item ml-auto" style="margin: 15px">
                    <img :src="tabDrawings[0].image" class="rounded" />
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
                  background: linear-gradient(186deg, rgba(238,241,209,0.6139589624912465) 0%, rgba(237,212,201,0.7568161053483894) 100%);   ">
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

            <p style="fontWeight: bold; marginBottom: 15px"> Si la majorité de ces dessins tournent autour du même sujet, c'est normal ! 
              Un de mes objectifs est de pouvoir être capable de créer des publicités animées pour mon jeu.
              Comme celà ne fait pas longtemps que je m'exerce dans ce domaine, j'essaie de m'améliorer sur un seul sujet.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { Tabs } from "@/components";
export default {
  components: {
    Tabs
  },
  bodyClass: "profile-page",
  data() {
    return {
      tabDrawings: [
        { image: require("@/assets/img/drawing/neon-fox.png") },
        { image: require("@/assets/img/drawing/fox-pumpkin.png") },
        { image: require("@/assets/img/drawing/andrew.png") },
        { image: require("@/assets/img/drawing/foxmoon.png") },
        { image: require("@/assets/img/drawing/github.png") },
        { image: require("@/assets/img/drawing/black-fox.png") },
        { image: require("@/assets/img/drawing/fox-silhouette1.png") },
        { image: require("@/assets/img/drawing/fox-silhouette2.png") },
        { image: require("@/assets/img/drawing/fox-sketch.png") },
        { image: require("@/assets/img/drawing/knight_full.png") },
        { image: require("@/assets/img/drawing/knight.png") },
        { image: require("@/assets/img/drawing/logo.png") },
        { image: require("@/assets/img/drawing/coyote.png") },
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
      default: require("@/assets/img/design.png")
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
