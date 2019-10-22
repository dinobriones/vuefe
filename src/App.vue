<template>
<v-app>

  <div v-if="$route.meta.logLayout">
      <router-view />
  </div>
  <div v-if="!$route.meta.logLayout">
    <NavSide />
    <NavTop />
    <v-content>
      <v-container fluid>
        <router-view></router-view>
      </v-container>
    </v-content>
    <v-footer clipped color="red">

    </v-footer>
  </div>
</v-app>
</template>
<script>
import NavSide from './views/layouts/NavSide.vue'
import NavTop from './views/layouts/NavTop.vue'
export default {
  components: {
     NavSide, NavTop
  }
  
}
</script>