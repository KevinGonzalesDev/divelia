<template>
  <v-app>
    <v-main class="d-flex align-center">
      <v-container fluid fill-height>
        <router-view />
      </v-container>

    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    //
  }),
}
</script>
