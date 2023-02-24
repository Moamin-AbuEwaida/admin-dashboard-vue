<template>
  <v-navigation-drawer :v-model="drawer" app>
    <v-img
      height="140"
      class="pa-4"
      src="https://images.unsplash.com/photo-1571171637578-41bc2dd41cd2?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8OHx8cHJvZ3JhbW1pbmd8ZW58MHx8MHx8&auto=format&fit=crop&w=400&q=60"
    >
      <div class="text-center">
        <v-avatar class="mb-4" color="grey darken-1" size="64">
          <v-img
            aspect-ratio="30"
            src="https://images.unsplash.com/photo-1633412802994-5c058f151b66?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=880&q=80"
          />
        </v-avatar>
        <h2 class="white--text">Web App</h2>
      </div>
    </v-img>
    <v-divider></v-divider>
    <v-list>
      <v-list-item v-for="[icon, text] in links" :key="icon" link>
        <v-list-item-icon>
          <v-icon>{{ icon }}</v-icon>
        </v-list-item-icon>

        <v-list-item-content>
          <v-list-item-title>{{ text }}</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
export default {
  name: "SideBar",
  props: ["drawer"],
  data() {
    return {
      links: [
        ["mdi-microsoft-windows", "Dashboard"],
        ["mdi-account", "Profile"],
        ["mdi-clipboard-list-outline", "Products"],
        ["mdi-card-account-details-outline", "Orders"],
        ["mdi-cog", "System Setting"],
      ],
    };
  },
};
</script>

<style scoped></style>
