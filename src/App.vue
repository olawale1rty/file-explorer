<template>
  <v-app>
    <v-app-bar
      app
      color=""
      dark
    >
      <div class="d-flex align-center">
      </div>

      <v-spacer></v-spacer>
    </v-app-bar>

    <v-main>
      <File/>
    </v-main>
  </v-app>
</template>

<script>
import File from './FileBrowser';

export default {
  name: 'App',

  components: {
    File,
  },

  data: () => ({
    //
  }),
};
</script>
