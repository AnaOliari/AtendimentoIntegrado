<template>
  <v-app theme="light">
    <v-main style="background: #e3f2fd">
      <v-container class="fill-height d-flex align-center justify-center">
        <div style="width: auto; height: auto" class="pr-10">
          <img src="@/assets/logo.png" alt="Logo" width="470" />
        </div>
        <div
          style="
            width: 540px;
            height: 330px;
            margin: 55px;
            background-color: #fafafa;
          "
          class="border rounded-lg pa-10 elevation-9"
        >
          <v-form>
            <h4>E-mail</h4>
            <v-responsive
              class="mx-auto elevation-4 border rounded-lg"
              max-width="auto"
              style="height: 50px; margin-bottom: 30px"
            >
              <v-textarea type="email" required></v-textarea>
            </v-responsive>
            <h4>Senha</h4>
            <v-responsive
              class="mx-auto elevation-4 border rounded-lg"
              max-width="auto"
              style="height: 50px; margin-bottom: 20px"
            >
              <v-text-field type="password" required></v-text-field>
            </v-responsive>

            <v-row justify="end">
              <v-col class="text-right">
                <a href="#" @click.prevent="forgotPassword">
                  <h4>Esqueceu sua senha?</h4></a
                >
              </v-col>
            </v-row>
            <v-btn
              class="elevation-9"
              style="height: 40px; width: 100px"
              color="primary"
              @click="login"
              ><h3>Entrar</h3></v-btn
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
