<template>
  <v-app id="inspire">
    <v-app-bar app>
      <div class="d-flex aling-center justify-center">
        <v-app-bar-nav-icon></v-app-bar-nav-icon>

        <h3 class="my-auto">Inscrição</h3>
      </div>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <v-container>
        <v-form>
          <v-row class="mt-0 pt-0">
            <v-col cols="12" sm="6">
              <v-text-field
                label="Nome"
                placeholder=""
                filled
                v-model="formData.name"
              ></v-text-field>
            </v-col>
            <v-col cols="12" sm="6">
              <v-text-field
                label="Sobrenome"
                placeholder=""
                filled
                v-model="formData.surname"
              ></v-text-field>
            </v-col>
          </v-row>
          <!--  -->
          <v-row class="mt-0 pt-0">
            <v-col cols="12" sm="6">
              <v-text-field
                label="Idade"
                placeholder=""
                filled
                v-model="formData.age"
              ></v-text-field>
            </v-col>
            <v-col cols="12" sm="6">
              <v-text-field
                label="Celular"
                placeholder=""
                filled
                v-model="formData.phone"
              ></v-text-field>
            </v-col>
          </v-row>
          <!--  -->
          <v-row class="mt-0 pt-0">
            <v-col cols="12" sm="6">
              <v-select
                :items="identitySexItems"
                label="Identidade de gênero"
                filled
                v-model="formData.sexIdentity"
              ></v-select>
            </v-col>
            <v-col cols="12" sm="6">
              <v-text-field
                label="E-mail"
                placeholder=""
                filled
                v-model="formData.email"
              ></v-text-field>
            </v-col>
          </v-row>
          <!--  -->
          [{{ formData }}]
          <v-row class="mt-0">
            <v-col>
              <v-btn class="d-flex ml-auto" color="success">Enviar</v-btn>
            </v-col>
          </v-row>
        </v-form>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  components: {},

  data: () => ({
    formData: {
      name: "",
      surname: "",
      age: "",
      phone: "",
      sexIdentity: "",
      email: "",
    },
    identitySexItems: [
      "Homem Cis",
      "Mulher Cis",
      "Mulher Transsexual",
      "Homem Transsexual",
      "Travesti",
      "Intersexo",
      "Cross dressing",
    ],
  }),
};
</script>
