<template>
  <div class="land">
    <div class="heroShoot">
      <h1 class="mainTitle">Teidesat 1A</h1>
      <h2 class="secondTitle">
        Shedding a light into infinite outter space 2B
      </h2>
    </div>
  </div>
  <div class="ksp my-5">
    <h2>Titular de apoyo previo 3B</h2>

    <!-- OBJETIVOS -->
    <div class="objectives">
      <div class="container">
        <div v-for="objective in objectives" :key="objective.index">
          <Objective
            :title="objective.title"
            :imgPosition="objective.imgPosition"
            :imgSrc="objective.imgSrc"
          ></Objective>
        </div>
      </div>
    </div>
    <h2>Texto de refuerzo general 1C</h2>

    <!-- TESTIMONIOS -->
    <div class="testimonies">
      <div class="container">
        <div class="row my-5">
          <div
            class="col-sm"
            v-for="testimony in testimonies"
            :key="testimony.index"
          >
            <Testimony
              :name="testimony.name"
              :imgSrc="testimony.imgSrc"
            ></Testimony>
          </div>
        </div>
      </div>
    </div>
  </div>
  <h2>Cierre de argumento 1D</h2>
  <div>
    <router-link to="/contacto" class="btn btn-primary px-4 py-3 bold">
      Contacto
    </router-link>
  </div>
</template>

<script>
// import LandPage from "@/components/LandPage.vue";
import Objective from "@/components/landpage/Objective.vue";
import Testimony from "@/components/landpage/Testimony.vue";

export default {
  name: "LandView",
  components: {
    Objective,
    Testimony,
  },
  data() {
    return {
      objectives: [
        {
          title: "Académico",
          imgPosition: "left",
          imgSrc: "logo_teidesat_negro.png",
        },
        {
          title: "Científico",
          imgPosition: "right",
          imgSrc: "logo_teidesat_negro.png",
        },
        {
          title: "Divulgativo",
          imgPosition: "left",
          imgSrc: "logo_teidesat_negro.png",
        },
        {
          title: "Investigativo",
          imgPosition: "right",
          imgSrc: "logo_teidesat_negro.png",
        },
      ],
      testimonies: [
        {
          name: "Fabio Bianchini",
          imgSrc: "ejemplo_testimonio.jpg",
        },
        {
          name: "Joshua Barrios Pérez",
          imgSrc: "ejemplo_testimonio.jpg",
        },
        {
          name: "Jorge Sierra Acosta",
          imgSrc: "ejemplo_testimonio.jpg",
        },
      ],
    };
  },
};
</script>
<style scoped>
.land {
  height: 100%;
}

.mainTitle {
  position: absolute;
  /* left: 0; */
  top: 45%;
  width: 100%;
  text-align: center;
  color: #032e43;
  font-size: 64px;
}
.secondTitle {
  color: #12638b;
  position: absolute;
  /* left: 0; */
  top: 60%;
  width: 100%;
  text-align: center;
}

.heroShoot {
  margin: 0;

  min-height: 100%;
  position: relative;
  /* opacity: 0.65; */
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  background-image: url(../assets/images/Fondo-Teidesat.png);
  font-family: "Nunito", sans-serif;
}
</style>
