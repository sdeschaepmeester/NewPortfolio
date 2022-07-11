<template>
  <div class="wrapper">
      <div class="section">
        <div class="container">
          <div class="md-layout">
            <div class="md-layout-item md-size-50 mx-auto">
              <div class="profile">
                <div class="avatar">
                </div>
                <div class="name">
                  <h3 class="title">Mentions légales</h3>
                </div>
              </div>
            </div>
          </div>
          <div class="description text-center">
            <div style="marginTop: 20%; backgroundColor: white; width: 120%">

Conformément aux dispositions des Articles 6-III et 19 de la Loi n°2004-575 du 21 juin 2004 pour la Confiance dans l'économie numérique, dite L.C.E.N., il est porté à la connaissance des utilisateurs et visiteurs du site Le Portfolio les présentes mentions légales.

 

Le site Le Portfolio est accessible à l'adresse suivante : www.le-portfolio.com (ci-après "le Site"). L'accès et l'utilisation du Site sont soumis aux présentes " Mentions légales" détaillées ci-après ainsi qu'aux lois et/ou règlements applicables.

La connexion, l'utilisation et l'accès à ce Site impliquent l'acceptation intégrale et sans réserve de l'internaute de toutes les dispositions des présentes Mentions Légales.

 

ARTICLE 1 - INFORMATIONS LÉGALES

En vertu de l'Article 6 de la Loi n° 2004-575 du 21 juin 2004 pour la confiance dans l'économie numérique, il est précisé dans cet article l'identité des différents intervenants dans le cadre de sa réalisation et de son suivi.

Le site Le Portfolio est édité par :

SAS POGO

ayant son siège social à l'adresse suivante : 6 rue de Lesdiguières 75004 Paris, et immatriculée au numéro suivant :420 700 817 00042.

Téléphone : 01 44 62 79 19

Adresse e-mail : contact@le-portfolio.com

ci après " l'Éditeur "

 

Le Directeur de publication est :

Denis Brunet

Adresse e-mail de contact : contact@le-portfolio.com

ci après " le Directeur de publication "

 

Le site Le Portfolio est hébergé par :

O.V.H.

dont le siège est situé à l'adresse suivante : 2 rue Kellermann - 59100 Roubaix - France.

Téléphone : 09 72 10 10 07

Adresse e-mail : support@ovh.com.

ci après " l'Hébergeur "

 

Sont considérés comme utilisateurs tout les internautes qui naviguent, lisent, visionnent et utilisent le site Le Portfolio.

ci après les " Utilisateurs "

 

ARTICLE 2 - ACCESSIBILITÉ

Le Site est par principe accessible aux utilisateurs 24/24h et 7/7j, sauf interruption, programmée ou non, pour des besoins de maintenance ou en cas de force majeure.

En cas d'impossibilité d'accès au Site, celui-ci s'engage à faire son maximum afin d'en rétablir l'accès. Le Site ne saurait être tenu pour responsable de tout dommage, quelle qu'en soit la nature, résultant de son indisponibilité.

 

ARTICLE 3 - COLLECTE DE DONNÉES ET LOI INFORMATIQUE ET LIBERTÉS

Ce site est déclaré à la Commission Nationale Informatique et Libertés (CNIL) sous le numéro 2005522.

En outre, il est conforme aux dispositions de la Loi 78-17 du 6 janvier 1978 relative à l'informatique, aux fichiers et aux libertés. En vertu de celle-ci l'Utilisateur bénéficie notamment d'un droit d'opposition (art. 32 et 38), d'accès (art. 38 et 39) et de rectification (art. 40) des données le concernant.

Pour faire usage de celui-ci, l'Utilisateur doit s'adresser à l'Éditeur en le contactant à l'adresse suivante : contact@le-portfolio.com, ou par courrier adressé au siège social de l'Éditeur en précisant ses nom, prénom(s), adresse et adresse(s) e-mail.

 

ARTICLE 4 - LOI APPLICABLE ET JURIDICTION

Les présentes Mentions Légales sont régies par la loi française. En cas de différend et à défaut d'accord amiable, le litige sera porté devant les tribunaux français conformément aux règles de compétence en vigueur.

 

ARTICLE 5 - CONTACT

Pour tout signalement de contenus ou d'activités illicites, l'Utilisateur peut contacter l'Éditeur à l'adresse suivante : contact@le-portfolio.com, ou par courrier recommandé avec accusé de réception adressé à l'Éditeur aux coordonnées précisées dans les présentes mentions légales.
          </div></div></div>
            
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
