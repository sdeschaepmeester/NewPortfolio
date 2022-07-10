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
                  <h3 class="title">Section Projets personnels</h3>
                </div>
              </div>
            </div>
          </div>
          <div class="description text-center">
            <p>
              Mes projets personnels
            </p>
          </div>
          <div class="profile-tabs">
            <p>Something</p>

          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  components: {
  },
  bodyClass: "profile-page",
  data() {
    return {
    };
  },
  props: {
    header: {
      type: String,
      default: require("@/assets/img/mill.png")
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
