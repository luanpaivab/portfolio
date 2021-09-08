<template>
  <div class="informations">
    <div class="jumbo">
      <b-avatar class="mx-3 my-3" src="https://media-exp1.licdn.com/dms/image/C4E03AQEJkpEEc9YJiA/profile-displayphoto-shrink_100_100/0/1629153607022?e=1636588800&v=beta&t=n1QFBHaoXcAbNR_focxUF7s6e65rQaViS9o5rAGlA0A" size="6rem"></b-avatar>
      <div class="intro">
        <h1>Luan Paiva Barbosa</h1>
        <h3>Desenvolvedor Full Stack | Node.js | Vue.Js</h3>
        <hr class="my-4" />
        <p style="font-weight: bold">
          Sou um desenvolvedor full stack que está em busca de entregar uma
          solução técnica <br />para um desafio de negócio.
        </p>
      </div>
    </div>
    <div class="container my-5">
      <b-row>
        <b-col sm="6">
          <div class="flex-container py-5">
            <span class="title-span">Conhecimentos</span>
            <b-col sm="12" class="main-card mt-2">
              <div
                class="card-container mr-2 mb-2"
                v-for="item in items"
                :key="item.language"
              >
                <div class="card-info py-1">
                  <img alt="Js" :src="item.src" />
                  <span class="display-flex px-1">{{ item.language }}</span>
                  <span class="time-span px-1">{{ item.time }}</span>
                </div>
              </div>
            </b-col>
          </div>
        </b-col>
        <b-col sm="6">
          <Experiences/>
        </b-col>
      </b-row>
    </div>
  </div>
</template>

<script>
import Experiences from "./Experiences.vue"
export default {
  name: "Informations",
  components:{ Experiences },
  data() {
    return {
      items: [
        {
          src: "https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-plain.svg",
          language: "JavaScript",
          time: "0 a 2 anos",
        },
        {
          src: "https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-plain.svg",
          language: "TypeScript",
          time: "0 a 1 ano",
        },
        {
          src: "https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg",
          language: "Node.Js",
          time: "0 a 2 anos",
        },
        {
          src: "https://raw.githubusercontent.com/devicons/devicon/master/icons/vuejs/vuejs-original.svg",
          language: "Vue.Js",
          time: "0 a 2 anos",
        },
        {
          src: "https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original.svg",
          language: "React.Js",
          time: "0 a 1 ano",
        },
        {
          src: "https://raw.githubusercontent.com/devicons/devicon/master/icons/bootstrap/bootstrap-plain.svg",
          language: "Bootstrap",
          time: "0 a 2 anos",
        },
        {
          src: "https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg",
          language: "HTML5",
          time: "0 a 2 anos",
        },
        {
          src: "https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg",
          language: "CSS3",
          time: "0 a 2 anos",
        },
      ],
    };
  },
  
};
</script>

<style>
.informations {
  padding: 20px;
}

.jumbo {
  /* width: 50%; */
  display: flex;
  /* justify-content: center; */
   background: url('https://wallpaperaccess.com/full/1877565.png') no-repeat center fixed;
  /* background-image: url(); */
  background-size: cover;
  padding-bottom: 20px;
  /* background-position: right bottom, left top; */
  /* background-repeat: no-repeat; */
}

.intro{
  display: flex;
  flex-direction: column;
  color: white;
  /* align-items: center; */
}

.flex-container {
  /* border: solid 1px #000; */
  border-radius: 5px;
  box-shadow: 0 1px 5px rgba(0, 0, 0, 0.5);
}

.title-span {
  /* background-color: tomato; */
  margin: 15px;
  font-size: 1.3rem;
  font-weight: bold;
  color: rgb(133, 133, 133);
}

.main-card {
  /* background-color: yellowgreen; */
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}
.card-container {
  /* background-color: tomato; */
  align-items: center;
  border: dashed 1px rgb(179, 179, 179);
  border-radius: 5px;
  font-size: 0.9rem;
}

.card-info {
  display: flex;
  flex-direction: row;
  align-items: center;
  font-weight: bold;
}

.card-info img {
  height: 30px;
  width: 40px;
}

.time-span {
  border-left: solid 1px rgb(179, 179, 179);
  color: rgb(117, 117, 117);
  /* padding-left: 5px; */
}

</style>