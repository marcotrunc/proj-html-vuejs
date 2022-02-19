<template>
  <div class="bs-black-lg">
    <!--Componente Header con all'interno logo e nav, l'altezza di questo blocco deve essere 100vh, ci sarà un bg-image, ed un sottoblocco  con un btn che sarà un componente da riciclare-->
    <Header :nav-items="navItems" />

    <!--Blocco con messaggio, fare triangolino in basso -->
    <Description />

    <!-- Blocco con due colonne, una contenente un immagine e l'altra un form con un button -->
    <Form />

    <Advantage />
    <!-- Blocco con quattro colonne, creare un componente e riperlo per quattro volte -->

    <Results />
    <!-- Qui ci sono due blocchi quasi identici. Titolo e icone uguali, cambia il contenuto del blocco, quindi fare lo stesso blocco ma con due contenuti diversi -->

    <Banner />

    <Trainers />
    <!-- Blocco simile ai due citati sopra con Titolo e icone uguali, ma con contenuto diverso. All'interno ci sono delle card da costituire come componenti e ripetere tre volte,STESSO BTN con quello di sotto  -->

    <div>
      <!-- Blocco simile ai due citati sopra con Titolo e icone uguali, ma con contenuto diverso. All'interno ci sono delle card da costituire come componenti e ripetere sei volte, per il BTN leggi sopra  -->
    </div>
    <section id="Footer">
      <div><!-- --></div>
      <div><!-- --></div>
      <div><!-- --></div>
    </section>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Description from "./components/Description.vue";
import Form from "./components/Form.vue";
import Advantage from "./components/Advantage.vue";
import Results from "./components/Results.vue";
import Banner from "./components/Banner.vue";
import Trainers from "./components/Trainers.vue";
export default {
  name: "App",
  components: {
    Header,
    Description,
    Form,
    Advantage,
    Results,
    Banner,
    Trainers,
  },
  data() {
    return {
      navItems: [
        "Home",
        "About us",
        "Facilities",
        "Membership",
        "Testimonials",
        "Blog",
      ],
    };
  },
};
</script>

<style lang="scss">
@import "./assets/scss/style.scss";
</style>
