<template>

    <v-app-bar fixed app color="#fcb69f" dark src="https://picsum.photos/1920/1080?random">
     <template v-slot:img="{ props }">
       <v-img v-bind="props" gradient="to top right, rgba(19,84,122,.5), rgba(128,208,199,.8)" />
     </template>

     <!-- <v-img src="./../../public/commsys.png" height="32" width="32"></v-img> -->

     <v-toolbar-title>
       <span class="font-weight-light display-1">Computer</span>
       <span class="display-1">Project</span>
     </v-toolbar-title>

     <div class="flex-grow-1"></div>

     <v-btn icon>
       <v-icon>mdi-magnify</v-icon>
     </v-btn>

     <v-btn icon :to="{ name: 'login' }" v-if="!loggedIn">
       <v-icon>warning</v-icon>
     </v-btn>

     <v-btn icon :to="{ name: 'about' }">
       <v-icon>notifications</v-icon>
     </v-btn>

     <v-btn icon>
       <v-icon>mdi-dots-vertical</v-icon>
     </v-btn>
    </v-app-bar>
</template>
<script>
export default {
    
}
</script>