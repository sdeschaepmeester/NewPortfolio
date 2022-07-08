<template>
  <div class="wrapper">
    <parallax
      class="section page-header header-filter"
      :style="headerStyle"
    ></parallax>
    <div class="main main-raised">
      <div class="section profile-content">
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
          <div class="profile-tabs">
             <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="4000"
      controls
      indicators
      background="#ababab"
      img-width="1024"
      img-height="480"
      style="text-shadow: 1px 1px 2px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <!-- Text slides with image -->
      <b-carousel-slide
        caption="First slide"
        text="Nulla vitae elit libero, a pharetra augue mollis interdum."
        img-src="https://picsum.photos/1024/480/?image=52"
      ></b-carousel-slide>

      <!-- Slides with custom text -->
      <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=54">
        <h1>Hello world!</h1>
      </b-carousel-slide>

      <!-- Slides with image only -->
      <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=58"></b-carousel-slide>

      <!-- Slides with img slot -->
      <!-- Note the classes .d-block and .img-fluid to prevent browser default image alignment -->
      <b-carousel-slide>
        <template #img>
          <img
            class="d-block img-fluid w-100"
            width="1024"
            height="480"
            src="https://picsum.photos/1024/480/?image=55"
            alt="image slot"
          >
        </template>
      </b-carousel-slide>

            <h5>Beaucoup de ces dessins représente un renard ou espèce proche; étant actuellement entrain de développer un jeu où le personnage principal
             est un renard, j'essaie de perfectionner mon style en dessinant les personnages de cet univers pour pouvoir un jour réaliser la promotion de mon jeu moi-même.
            </h5>

            <tabs
              :tab-name="['Dessins', 'Animations', 'En cours']"
              :tab-icon="['palette', 'movie', 'draw']"
              plain
              nav-pills-icons
              color-button="success"
            >
              <!-- here you can add your content for tab-content -->
              <template slot="tab-pane-1">
                <div class="md-layout">
                  <div class="md-layout-item  ml-auto">
                    <img :src="tabPane1[0].image" class="rounded" />
                    <img :src="tabPane1[1].image" class="rounded" />
                    <img :src="tabPane1[2].image" class="rounded" />
                    <img :src="tabPane1[3].image" class="rounded" />
                  </div>
                  <div class="md-layout-item md-size-50 ml-auto">
                    <img :src="tabPane1[4].image" class="rounded" />
                    <img :src="tabPane1[5].image" class="rounded" />
                                        <img :src="tabPane1[6].image" class="rounded" />
                    <img :src="tabPane1[7].image" class="rounded" />

                  </div>
                </div>
              </template>
              <template slot="tab-pane-2">
                <div class="md-layout">
                  <div class="md-layout-item md-size-25 ml-auto">
                    <img :src="tabPane2[0].image" class="rounded" />
                    <img :src="tabPane2[1].image" class="rounded" />
                    <img :src="tabPane2[2].image" class="rounded" />
                  </div>
                  <div class="md-layout-item md-size-25 mr-auto">
                    <img :src="tabPane2[3].image" class="rounded" />
                    <img :src="tabPane2[4].image" class="rounded" />
                  </div>
                </div>
              </template>
              <template slot="tab-pane-3">
                <div class="md-layout">
                  <div class="md-layout-item md-size-25 ml-auto">
                    <img :src="tabPane3[0].image" class="rounded" />
                    <img :src="tabPane3[1].image" class="rounded" />
                  </div>
                  <div class="md-layout-item md-size-25 mr-auto">
                    <img :src="tabPane3[2].image" class="rounded" />
                    <img :src="tabPane3[3].image" class="rounded" />
                    <img :src="tabPane3[4].image" class="rounded" />
                  </div>
                </div>
              </template>
            </tabs>
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
      tabPane1: [
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
      tabPane2: [
        { image: require("@/assets/img/animation/dog_computer.gif") },
        { image: require("@/assets/img/animation/fox_painting.gif") },
        { image: require("@/assets/img/animation/fox_first_anim.gif") },
        { image: require("@/assets/img/animation/fox_shelf.gif") },
        { image: require("@/assets/img/animation/fox_munching.gif") },
      ],
      tabPane3: [
        { image: require("@/assets/img/examples/mariya-georgieva.jpg") },
        { image: require("@/assets/img/examples/studio-3.jpg") },
        { image: require("@/assets/img/examples/clem-onojeghuo.jpg") },
        { image: require("@/assets/img/examples/olu-eletu.jpg") },
        { image: require("@/assets/img/examples/studio-1.jpg") }
      ]
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
