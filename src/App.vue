<template>
  <div>
    <!--Componente Header con all'interno logo e nav, l'altezza di questo blocco deve essere 100vh, ci sarà un bg-image, ed un sottoblocco  con un btn che sarà un componente da riciclare-->
    <Header :nav-items="navItems" />

    <Description />
    <!--Blocco con messaggio, fare triangolino in basso -->
    <div>
      <!-- Blocco con due colonne, una contenente un immagine e l'altra un form con un button -->
    </div>
    <div>
      <!-- Blocco con quattro colonne, creare un componente e riperlo per quattro volte -->
    </div>
    <div>
      <!-- Qui ci sono due blocchi quasi identici. Titolo e icone uguali, cambia il contenuto del blocco, quindi fare lo stesso blocco ma con due contenuti diversi -->
    </div>
    <div><!--Leggere Sopra --></div>
    <div><!--Jumbo --></div>
    <div>
      <!-- Blocco simile ai due citati sopra con Titolo e icone uguali, ma con contenuto diverso. All'interno ci sono delle card da costituire come componenti e ripetere tre volte,STESSO BTN con quello di sotto  -->
    </div>
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
export default {
  name: "App",
  components: { Header, Description },
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
