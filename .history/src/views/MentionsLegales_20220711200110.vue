<template>
  <div class="wrapper">
      <div class="section">
        <div class="container">
          <div>
            <div style="marginTop: 20%; backgroundColor: white; width: 95%; 
            box-shadow: 1px 1px 10px 1px #154d1a;">
            <div style="margin: 20px">
            <h2 style="textAlign: center">Mentions légales</h2>
            <h3>1 - Édition du site</h3>

            En vertu de l'article 6 de la loi n° 2004-575 du 21 juin 2004 pour la confiance dans l'économie numérique, il est précisé aux utilisateurs du site internet https://deschaepmeester-samantha.surge.sh l'identité des différents intervenants dans le cadre de sa réalisation et de son suivi:
            <br/><br/>

            Propriétaire du site : <span style="fontWeight: bold">Deschaepmeester Samantha</span> - Contact : <span style="fontWeight: bold">deschaepmeester.samantha@gmail.com</span> - Adresse : France.
            <br/>

            Ce site web est un portfolio ayant pour n'ayant pas de but pécunier. De plus, aucune donnée supplémentaire n'est demandé aux utilisateurs.
            <br/><br/>

            Hébergeur : Surge https://surge.sh/
            <br/>

            Délégué à la protection des données : <span style="fontWeight: bold">Samantha Deschaepmeester - deschaepmeester.samantha@gmail.com</span>
            <br/><br/>

            Autres contributeurs : 
            <br/>
            - Tim creative (https://www.creative-tim.com/) pour le template VueJS disponible à l'adresse suivante : https://demos.creative-tim.com/vue-material-kit/?_ga=2.224804371.885857106.1657287321-1852356776.1650483914#/ 
            <br/>
            - Surge (https://surge.sh/) pour le déploiement du présent site web.
            <br/>

            <h3>2 - Propriété intellectuelle et contrefaçons.</h3>

            Le présent site web a été réalisé par le biais d'un modèle gratuit proposé par Tim Creative et adapté au besoin de son propriétaire.
            <br/>
            La licence concernant l'utilisation du modèle Tim Creative peut se retrouver <a href="https://www.creative-tim.com/license?_ga=2.51012329.1549389931.1657556868-1852356776.1650483914">en cliquant sur ce lien.</a>
            <br/><br/>

            Deschaepmeester Samantha est propriétaire des droits de propriété intellectuelle et détient les droits d’usage sur les éléments accessibles sur le site internet : textes, images, graphismes, logos, vidéos.
            <br/><br/>
            Tout projet extérieur mentionné dans ce site ayant pour propriétaire Deschaepmeester Samantha est soumis à cette même propriété intellectuelle et il est interdit de reproduire, modifier, publier ces éléments.
            <br/><br/>
            <span style="fontWeight: bold">
            Toute reproduction, représentation, modification, publication, adaptation d'un de ces éléments du site, quel que soit le moyen ou le procédé utilisé, est interdite, sauf autorisation écrite préalable de Deschaepmeester Samantha.
            <br/><br/>
            Toute exploitation non autorisée du site ou de l’un quelconque des éléments qu’il contient sera considérée comme constitutive d’une contrefaçon et poursuivie conformément aux dispositions des articles L.335-2 et suivants du Code de Propriété Intellectuelle.
            </span>

            <br/>

            <h3>3 - Limitations de responsabilité.</h3>

            Deschaepmeester Samantha ne pourra être tenu pour responsable des dommages directs et indirects causés au matériel de l’utilisateur, lors de l’accès au site https://deschaepmeester-samantha.surge.sh.
            <br/>
            Deschaepmeester Samantha décline toute responsabilité quant à l’utilisation qui pourrait être faite des informations et contenus présents sur https://deschaepmeester-samantha.surge.sh.
            <br/>
            Deschaepmeester Samantha s’engage à sécuriser au mieux le site https://deschaepmeester-samantha.surge.sh, cependant sa responsabilité ne pourra être mise en cause si des données indésirables sont importées et installées sur son site à son insu.

            <h3>4 - CNIL et gestion des données personnelles.</h3>

            Conformément aux dispositions de la loi 78-17 du 6 janvier 1978 modifiée, l’utilisateur du site https://deschaepmeester-samantha.surge.sh dispose d’un droit d’accès, de modification et de suppression des informations collectées. 
            <br/>
            Pour exercer ce droit, envoyez un message à notre Délégué à la Protection des Données : Samantha Deschaepmeester - deschaepmeester.samantha@gmail.com.
            <br/>
            Nous ne traitons aucune donnée supplémentaire. Si jamais une modification devait être effectuée, nos utilisateurs en seront informé.

            <h3>5 - Liens hypertextes et cookies</h3>

            Le site https://deschaepmeester-samantha.surge.sh contient des liens hypertextes vers d’autres sites et dégage toute responsabilité à propos de ces liens externes ou des liens créés par d’autres sites vers https://deschaepmeester-samantha.surge.sh.
            <br/><br/>
            La navigation sur le site https://deschaepmeester-samantha.surge.sh est susceptible de provoquer l’installation de cookie(s) sur l’ordinateur de l’utilisateur.
            <br/><br/>
            Un <span style="fontWeight: bold">"cookie"</span> est un fichier de petite taille qui enregistre des informations relatives à la navigation d’un utilisateur sur un site. Les données ainsi obtenues permettent d'obtenir des mesures de fréquentation, par exemple.
            <br/><br/>
            Vous avez la possibilité d’accepter ou de refuser les cookies en modifiant les paramètres de votre navigateur. Aucun cookie ne sera déposé sans votre consentement.

            <h3>6 - Droit applicable et attribution de juridiction.</h3>

            Tout litige en relation avec l’utilisation du site https://deschaepmeester-samantha.surge.sh est soumis au droit français. 
            <br/><br/>
            En dehors des cas où la loi ne le permet pas, il est fait attribution exclusive de juridiction aux tribunaux compétents de <span style="fontWeight: bold">Pontoise</span>.
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

p{
    font-size: 10!important;
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
