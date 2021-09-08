<template>
  <v-app id="inspire">
    <v-navigation-drawer
      v-model="drawer"
      app
      :mini-variant.sync="mini"
      permanent
    >
      <v-list-item class="px-2">
        <v-list-item-avatar @click.stop="mini = !mini">
          <v-img src="../assets/perfil.jpg"></v-img>
        </v-list-item-avatar>

        <v-list-item-title>Luan Paiva</v-list-item-title>

        <!-- <v-btn
          icon
          @click.stop="mini = !mini"
        >
          <v-icon>mdi-chevron-left</v-icon>
        </v-btn> -->
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense>
        <v-list-item v-for="item in items" :key="item.title" link>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar app>
      <v-app-bar-nav-icon @click.stop="mini = !mini"></v-app-bar-nav-icon>

      <v-toolbar-title>Portfólio</v-toolbar-title>
    </v-app-bar>

    <v-main>
      <Informations/>
    </v-main>
  </v-app>
</template>

<script>
import Informations from "./Informations.vue";

export default {
  components: { Informations  },
  data: () => ({
    drawer: null,
    items: [
      { title: "Home", icon: "mdi-home-city" },
      { title: "My Account", icon: "mdi-account" },
      { title: "Users", icon: "mdi-account-group-outline" },
    ],
    mini: true,
  }),
};
</script>
<style>
 #inspire{
   min-height: 120vh;
   background-color: rgba(243, 243, 243, 0.74);
 }
</style>