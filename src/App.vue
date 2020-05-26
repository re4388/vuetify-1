<template>
  <v-app>
    <v-card width="400px" class="mt-5 mx-a">
      <v-card-title class="pb-0">
        <h1>Login</h1>
      </v-card-title>

      <v-card-text>
        <v-form>
          <v-text-field label="Username" prepend-icon="mdi-account-circle" />

          <v-text-field
            :type="showPassword ? 'text' : 'password'"
            label="Password"
            prepend-icon="mdi-lock"
            :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
            @click:append="showPassword = !showPassword"
          />
        </v-form>
      </v-card-text>
      <v-divider></v-divider>
      <v-card-actions>
        <v-btn color="success">Register</v-btn>
        <v-spacer></v-spacer>
        <v-btn color="info">Login</v-btn>
      </v-card-actions>
    </v-card>
    <v-container fluid>
      <v-row align="center">
        <v-col class="d-flex" cols="12" sm="6">
          <v-select :items="items" label="this is label"></v-select>
        </v-col>

        <v-col class="d-flex" cols="12" sm="6">
          <v-select :items="items" filled label="Filled style"></v-select>
        </v-col>

        <v-col class="d-flex" cols="12" sm="6">
          <v-select :items="items" label="Outlined style" outlined></v-select>
        </v-col>

        <v-col class="d-flex" cols="12" sm="6">
          <v-select :items="items" label="Solo field" solo></v-select>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>


<script>
export default {
  name: "App",
  data() {
    return {
      showPassword: false,
      items: ["Foo", "Bar", "Fizz", "Buzz"]
    };
  }
};
</script>