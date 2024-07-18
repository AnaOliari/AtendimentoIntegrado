<template>
  <v-app theme="light">
    <v-main style="background: #e3f2fd">
      <v-container class="fill-height d-flex align-center justify-center">
        <div style="width: auto; height: auto" class="pr-10">
          <img src="@/assets/logo.png" alt="Logo" width="800" />
        </div>
        <div
          style="
            width: 700px;
            height: 400px;
            margin: 50px;
            background-color: #fafafa;
          "
          class="border rounded-lg pa-12 elevation-9"
        >
          <v-form>
            <h3>E-mail</h3>
            <v-responsive
              class="mx-auto elevation-4 border rounded-lg"
              max-width="auto"
              style="height: 57px; margin-bottom: 30px"
            >
              <v-textarea type="email" required></v-textarea>
            </v-responsive>
            <h3>Senha</h3>
            <v-responsive
              class="mx-auto elevation-4 border rounded-lg"
              max-width="auto"
              style="height: 57px; margin-bottom: 20px"
            >
              <v-text-field type="password" required></v-text-field>
            </v-responsive>

            <v-row justify="end">
              <v-col class="text-right">
                <a href="#" @click.prevent="forgotPassword">
                  <h3>Esqueceu-se da sua senha?</h3></a
                >
              </v-col>
            </v-row>
            <v-btn
              style="height: 50px; width: 160px"
              color="primary"
              @click="login"
              ><h2>Entrar</h2></v-btn
            >
          </v-form>
        </div>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      email: "",
      password: "",
    };
  },
  methods: {
    login() {
      console.log("Email:", this.email);
      console.log("Senha:", this.password);
    },
    forgotPassword() {
      console.log("Recuperar senha");
    },
  },
};
</script>

<style></style>
