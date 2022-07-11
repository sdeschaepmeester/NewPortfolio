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
          <h4>My pet fox</h4>
          <div class="md-layout">
            <div class="md-layout-item md-size-50 md-xsmall-size-100" >
              <div style="box-shadow: 1px 1px 10px 1px #154d1a;">
                <img
                  :src="require('@/assets/img/livingroom.png')"
                />
              </div>
            </div>
            <div class="md-layout-item md-xsmall-size-100">
              <p><span style="fontWeight: bold">Date de début :</span> Juillet 2021</p>
              <p><span style="fontWeight: bold">État :</span> En cours (~ 85% fini)</p>
              <p><span style="fontWeight: bold">Technologies :</span> React-native, Expo (développement), Canva (design)</p>
              <p>My pet fox est un jeu mobile que je réalise entièrement par mes moyens. Tous les pixels arts, animations et bien
                sûr le code sont le fruit de mon travail.
                <br/><br/>
                Ce jeu mobile est un jeu gratuit qui sera disponible sur Android et IOS sans nécessité de connexion. 
                Vous vous occuperez d'un renard, et intéragissez avec son monde; jouer à des minis-jeux, débloquer des événements...
              </p>
            </div>
          </div>
            <div class="alert alert-success" style="marginTop: 5%" >
              <div class="container">
                <b>Pour en voir plus</b> : J'ai réalisé une playlist de vidéos de mon jeu. La playlist
                est disponible <a href="https://www.youtube.com/watch?v=EwmwHKwsFOw&list=PLVTOiOamTkwKNusnK4w8eav7kWht3L8ZN" class="linkClick" >en cliquant sur ce lien.</a>
              </div>
            </div>
          </div>


          <h4 style="marginTop: 5%">Mon portfolio</h4>
          <div class="md-layout">
            <div class="md-layout-item md-size-50 md-xsmall-size-100" >
              <div style="box-shadow: 1px 1px 10px 1px #154d1a;">
                <img
                  :src="require('@/assets/img/wallpaper.png')"
                />
              </div>
            </div>
            <div class="md-layout-item md-xsmall-size-100" style="marginBottom: 5%">
              <p><span style="fontWeight: bold">Date de début :</span> Juin 2022</p>
              <p><span style="fontWeight: bold">État :</span> Terminé</p>
              <p><span style="fontWeight: bold">Technologies :</span> VueJS, Template by Tim creative</p>
              <p>Anciennement fait en ReactJS, j'ai décidé de refaire un projet de portfolio en utilisant du VueJS.
                <br/><br/>
                Ce portfolio est composé de plusieurs sections : CV, Design, Projet personnels.
                <br/><br/>
                Toutes les images et animations présentes dans ce portfolio m'appartiennent et ont été réalisés sous FireAlpaca.
              </p>
            </div>
          </div>
          <br/>
          <p>
            D'autres projets verront le jour, mais ne sont pour le moment qu'au stade de l'idée.
            Je préfère me focaliser sur un projet, et le finir avant d'en commencer un autre.
          </p>
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
.linkClick{
  color: white!important;
  text-decoration: underline!important;
}
.linkClick:hover{
  font-weight: bold!important;
  text-decoration: underline!important;
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
