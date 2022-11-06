<!--Login Angelica-->
<template>
  <div>
    <div class="home-nav">
      <div class="container row">
         <!-- Las imagenes deben ser recortadas y actualizadas -->
        <img class=" col-md-2 col-sm-4 col-3 ms-5" src="../assets/img/Logo-Dark-Clip.jpg" alt="Logo" />
      </div>
    </div>


    <div class="login text-center">
      <!-- Las imagenes deben ser recortadas y actualizadas -->
      <img class="logo-hero" src="../assets/img/Logo-White-Clip.jpg" alt="Foto-Hero">

      <LoginFormComponent></LoginFormComponent>

    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import LoginFormComponent from "../components/LoginFormComponent.vue";

export default {
  name: "HomeView",
  components: {
    LoginFormComponent
  }
};
</script>

<style scoped>
.home-nav {
  position: absolute;
  width: 100%;
  background: #1F2D4A;
  z-index: 2;
}

.logo-hero {
  max-width: 350px;
  margin-top: 10rem;
  margin-bottom: 2rem;
}

</style>
