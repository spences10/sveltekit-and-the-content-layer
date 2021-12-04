<template>
  <v-clicks>
    <img class="drupal" src="/assets/drupal.png" alt="drupal logo" />
    <img
      class="wordpress"
      src="/assets/wordpress.png"
      alt="wordpress logo"
    />
    <img
      class="aem"
      src="/assets/adobe-experience-manager.png"
      alt="adobe experience manager logo"
    />
  </v-clicks>
</template>

<style scoped>
.drupal {
  position: absolute;
  left: 130px;
  top: 100px;
  width: 20%;
}
.wordpress {
  position: absolute;
  left: 540px;
  top: 60px;
  width: 20%;
}
.aem {
  position: absolute;
  left: 380px;
  top: 300px;
  width: 20%;
}
.slidev-vclick-target {
  transition: opacity 400ms ease;
}
</style>
