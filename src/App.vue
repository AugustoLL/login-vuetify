<template>
  <v-app>
    <v-content>
      <v-card width="400" class="mx-auto mt-10" dark>
        <v-card-title class="pt-10 pb-5 red accent-2">
          <h1 class="mx-auto black--text">
            <v-icon color="black" x-large>mdi-vuetify</v-icon>Login
          </h1>
        </v-card-title>
        <v-card-text class="px-10 py-3">
          <v-form>
            <v-text-field label="Username" prepend-icon="mdi-account-circle"></v-text-field>
            <v-text-field 
              label="Password" 
              prepend-icon="mdi-key" 
              :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'" 
              :type="showPassword ? 'text' : 'password'"
              @click:append="showPassword = !showPassword"
            ></v-text-field>
          </v-form>
        </v-card-text>
        <v-divider></v-divider>
        <v-card-actions class="px-10 py-3">
          <v-btn color="red accent-2">Register</v-btn>
          <v-spacer></v-spacer>
          <v-btn color="secondary">Login</v-btn>
        </v-card-actions>
      </v-card>
    </v-content>
  </v-app>
</template>

<script>

export default {
  name: 'App',
  components: {
  },

  data: () => ({
    showPassword: false,
  }),
};
</script>
