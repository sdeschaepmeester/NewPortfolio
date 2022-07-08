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
                  <img
                    :src="img"
                    alt="Circle Image"
                    class="img-raised rounded-circle img-fluid"
                  />
                </div>
                <div class="name">
                  <h3 class="title">Samantha deschaepmeester</h3>
                  <h6>Développeuse web et mobile</h6>
                  <md-button
                    href="https://www.linkedin.com/in/samantha-deschaepmeester/"
                    class="md-just-icon md-simple md-dribbble"
                    ><i class="fab fa-linkedin"></i></md-button>
                  <md-button
                    href="https://github.com/sdeschaepmeester"
                    class="md-just-icon md-simple md-twitter"
                    ><i class="fab fa-github"></i></md-button>
                  <md-button
                    href="https://www.youtube.com/channel/UC_iJU8cmp9euihl1_mgpZ0g"
                    class="md-just-icon md-simple md-pinterest"
                    ><i class="fab fa-youtube"></i
                  ></md-button>
                </div>
              </div>
            </div>
          </div>
          <div class="description text-center">
            <p>
              Passionnée par le développement et l'informatique, j'aime apprendre de nouvelles technologies web ou mobile.
              Si j'ai choisi le domaine du développement informatique, c'est que les possibilités de création sont presque infinis.
            </p>
          </div>
          <div>
            <img
                :src="cvimg"
                alt="Retrouvez mon CV ici : https://www.linkedin.com/in/samantha-deschaepmeester/"
                class="img-raised img-fluid"
            />
            <br/>
            <h3>Retototoro</h3>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  bodyClass: "profile-page",
  props: {
    header: {
      type: String,
      default: require("@/assets/img/linkedin-banner.png")
    },
    img: {
      type: String,
      default: require("@/assets/img/faces/me.png")
    },
    cvimg: {
      type: String,
      default: require("@/assets/img/CV_Deschaepmeester_Samantha.png")
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
