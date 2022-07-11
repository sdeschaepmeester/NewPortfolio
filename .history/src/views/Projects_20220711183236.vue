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
                  <h3 class="title" style="color: white" >Projets personnels</h3>
                </div>
              </div>
            </div>
          </div>
          <div class="description text-center">
            <p>
              Durant mon temps libre, je travaille beaucoup sur des projets personnels et ainsi monter en compétences.
            </p>
          </div>
          <div class="profile-tabs">

      <div class="md-layout">
        <div
          class="md-layout-item md-size-20 md-xsmall-size-100"
        >
          <img
            :src="require('@/assets/img/drawing/neon-fox.png')"
          />
        </div>
        <div
          class="md-layout-item md-size-20 md-xsmall-size-100"
        >
          <h4>My pet fox</h4>
          <p>Date de début : Juillet 2021</p>
          <p>État : En cours (~ 85% fini)</p>
          
        </div>
      </div>






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
  },
  computed: {
    headerStyle() {
      return {
        backgroundImage: `url(${this.header})`
      };
    }
  },
  methods: {
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
