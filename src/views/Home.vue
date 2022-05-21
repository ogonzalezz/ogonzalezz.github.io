<template>
  <b-container fluid>
    <b-row
      align-v="center"
      align-h="center"
      class="row1"
      id="homeSection"
      cols="1"
    >
      <b-col>
        <b-row cols="1">
          <b-col sm="8" class="text-center">
            <h1>
              ÓSCAR <br />
              GONZÁLEZ
            </h1>
          </b-col>
          <b-col sm="4">
            <div class="grid" style="position: relative">
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem"></div>
              <div class="gridItem2">{{ data[0].elements[0].el1 }}</div>
            </div>
            <!--             <img
              src="../assets/palmtree.svg"
              alt=""
              height="100%"
              class="palmtree"
            /> -->
          </b-col>
        </b-row>
      </b-col>
      <b-col align-self="start">
        <b-button class="cta" href="#contactSection">{{
          data[0].elements[0].el2
        }}</b-button>
      </b-col>
    </b-row>
    <hr />
    <b-container>
      <b-row
        id="aboutSection"
        class="mt-4 row2"
        align-v="center"
        cols="1"
        cols-sm="2"
        v-scrollanimation
      >
        <b-col>
          <div class="text-left">
            <h2 class="pb-4">
              <img src="../assets/dado1.svg" alt="" height="55vh" />
              {{ data[0].elements[0].el3 }}
            </h2>
            <p>{{ data[0].elements[0].el4 }}</p>
            <b-button class="cvButton" href="./avatar.png" download>{{
              data[0].elements[0].el5
            }}</b-button>
            <!-- <a href="./avatar.png" download>
            <button type="button">Download</button>
          </a> -->
          </div>
        </b-col>
        <b-col>
          <div>
            <img
              src="../assets/me.png"
              alt=""
              class="avatarImage"
              width="100%"
            />
          </div>
        </b-col>
      </b-row>
      <hr />
      <b-row
        id="skillsSection"
        class="mt-4 row3"
        align-v="center"
        cols="1"
        cols-sm="2"
        v-scrollanimation
      >
        <b-col>
          <div class="text-left">
            <h2 class="pb-4">
              <img src="../assets/dado2.svg" alt="" height="55vh" />
              {{ data[0].elements[0].el6 }}
            </h2>
            <p>{{ data[0].elements[0].el7 }}</p>
            <b-row>
              <b-col
                cols="3"
                sm="2"
                v-for="(section, index) in sections"
                :key="section.name"
                @click="changeSection(index)"
              >
                <div
                  style="
                    background-color: #ffc0ad;
                    border-radius: 10px;
                    padding: 10px;
                    width: 60px;
                  "
                >
                  <img :src="section.image" alt="" width="100%" />
                </div>
              </b-col>
            </b-row>
            <!-- <a href="./avatar.png" download>
            <button type="button">Download</button>
          </a> -->
          </div>
        </b-col>
        <b-col>
          <div>
            <b-container class="bv-example-row">
              <b-row>
                <b-col
                  cols="5"
                  md="4"
                  v-for="element in sections[selectedSection].elements"
                  :key="element.name"
                >
                  <div
                    class="m-4"
                    style="
                      background-color: #ffc0ad;
                      border-radius: 10px;
                      padding: 10px;
                      width: 60px;
                    "
                  >
                    <img
                      :src="element.image"
                      alt=""
                      width="100%"
                      v-b-tooltip.hover
                      :title="element.name"
                    />
                  </div>
                </b-col>
              </b-row>
            </b-container>
          </div>
        </b-col>
      </b-row>
      <hr />
      <b-row
        id="ProjectsSection"
        class="mt-4 row4"
        align-v="center"
        cols="1"
        cols-sm="2"
        v-scrollanimation
      >
        <b-col>
          <div class="text-left">
            <h2 class="pb-4">
              <img src="../assets/dado3.svg" alt="" height="55vh" />
              {{ data[0].elements[0].el10 }}
            </h2>
            <p>{{ data[0].elements[0].el11 }}</p>
          </div>
        </b-col>
        <b-col>
          <div>
            <b-carousel
              id="carousel-fade"
              style="text-shadow: 0px 0px 2px #000"
              fade
              controls
              indicators
              img-width="1024"
              img-height="480"
            >
              <a
                href="https://github.com/OscarCastellaSanSegundo/Project2"
                target="_blank"
              >
                <b-carousel-slide
                  img-src="../assets/jsGame.gif"
                  style="border-radius: 20px"
                ></b-carousel-slide>
              </a>
              <a
                href="https://github.com/OscarCastellaSanSegundo/Project2"
                target="_blank"
              >
                <b-carousel-slide
                  img-src="../assets/health.gif"
                  style="border-radius: 20px"
                ></b-carousel-slide>
              </a>
              <a href="https://movieapp-mpf8.onrender.com" target="_blank">
                <b-carousel-slide
                  img-src="../assets/movieApp.gif"
                  style="border-radius: 20px"
                ></b-carousel-slide>
              </a>
            </b-carousel>
          </div>
        </b-col>
      </b-row>
      <hr />
      <b-row
        id="contactSection"
        class="mt-4 contactInfo row5"
        align-v="center"
        cols="1"
        cols-sm="2"
        v-scrollanimation
      >
        <b-col class="text-left">
          <div>
            <h2>
              <img src="../assets/logo2.svg" alt="" height="55vh" />
              {{ data[0].elements[0].el12 }}
            </h2>
          </div>
          <div class="mt-4">
            <h3>{{ data[0].elements[0].el13 }}</h3>
            <p>Montcada i Reixac, Barcelona</p>
          </div>
          <div>
            <h3>{{ data[0].elements[0].el14 }}</h3>
            <p>727735532</p>
          </div>
          <div>
            <h3>Email</h3>
            <p>opt3.oscar@gmail.com</p>
          </div>
          <div>
            <h3>{{ data[0].elements[0].el15 }}</h3>
            <b-container class="bv-example-row">
              <b-row>
                <b-col
                  cols="3"
                  sm="2"
                  v-for="element in socialMedia[0].elements"
                  :key="element.name"
                >
                  <div
                    style="
                      background-color: #ffc0ad;
                      border-radius: 10px;
                      padding: 10px;
                      width: 60px;
                    "
                  >
                    <a :href="element.link" target="_blank">
                      <img :src="element.image" alt="" width="100%" />
                    </a>
                  </div>
                </b-col>
              </b-row>
            </b-container>
          </div>
        </b-col>
        <b-col align-h="center" class="mt-5">
          <b-card
            style="max-width: 20rem; border: none; border-radius: 20px"
            class="mx-auto mb-2"
          >
            <form
              target="_blank"
              action="https://formsubmit.co/opt3.oscar@gmail.com"
              method="POST"
            >
              <input
                type="hidden"
                name="_next"
                value="https://oscargonzalez.onrender.com/"
              />
              <input type="hidden" name="_captcha" value="false" />
              <div class="mt-2">{{ data[0].elements[0].el16 }}</div>
              <b-form-input
                placeholder="e.g. John Doe"
                required
                name="name"
              ></b-form-input>
              <div class="mt-2">Email</div>
              <b-form-input
                placeholder="Enter your name"
                required
                name="email"
              ></b-form-input>
              <div class="mt-2">{{ data[0].elements[0].el17 }}</div>
              <b-form-textarea
                id="textarea"
                placeholder="Enter something..."
                rows="5"
                required
                name="message"
              ></b-form-textarea>
              <b-button
                type="submit"
                style="background-color: #e68a6e"
                class="mt-2"
                >Send</b-button
              >
            </form>
          </b-card>
        </b-col>
      </b-row>
    </b-container>
  </b-container>
</template>

<script>
/* import SkillsCard from "@/components/SkillsCard.vue"; */
/* import Cube3d from "@/components/Cube3d.vue"; */
/* import FooterLanding from "@/components/FooterLanding.vue"; */
export default {
  name: "Home",
  mounted() {
    this.$root.$on("message", (msg) => {
      console.log(msg);
    });
  },
  components: {
    /* "skills-card": SkillsCard, */
    /* "cube-3d": Cube3d, */
    /* "footer-landing": FooterLanding, */
  },
  data() {
    return {
      data: [
        {
          id: "0",
          lang: "english",
          elements: [
            {
              el1: "TAP",
              el2: "GET IN TOUCH",
              el3: "ABOUT ME",
              el4: "Here you have a video where you can know me better.",
              el5: "GET MY CV",
              el6: "MY SKILLS",
              el7: "This is my current knowledge but I never stop learning!",
              el8: "LANGUAGES",
              el9: "TOOLS",
              el10: "MY PROJECTS",
              el11: "Here are some of the projects I've done.",
              el12: "DO YOU WANT US TO WORK TOGETHER?",
              el13: "Address",
              el14: "Social media",
              el15: "Name",
              el16: "Message",
              el17: "Send",
            },
          ],
        },
        {
          id: "1",
          lang: "español",
          elements: [
            {
              el1: "TOCA",
              el2: "PONTE EN CONTACTO",
              el3: "SOBRE MÍ",
              el4: "Aquí tienes un vídeo donde me puedes conocer mejor",
              el5: "DESCARGA MI CV",
              el6: "MIS HABILIDADES",
              el7: "Estos son mis conocimientos actuales, ¡pero nunca dejo de aprender!",
              el8: "LENGUAJES",
              el9: "HERRAMIENTAS",
              el10: "MIS PROYECTOS",
              el11: "Estos son algunos de los proyectos que he hecho",
              el12: "¿QUIERES QUE TRABAJEMOS JUNTOS?",
              el13: "Dirección",
              el14: "Redes sociales",
              el15: "Nombre",
              el16: "Mensaje",
              el17: "Enviar",
            },
          ],
        },
        {
          id: "2",
          lang: "català",
          elements: [
            {
              el1: "TOCA",
              el2: "POSA'T EN CONTACTE",
              el3: "SOBRE MÍ",
              el4: "Aquí tens un video on em pots conéixer millor",
              el5: "DESCARREGA EL MEU CV",
              el6: "LES MEVES HABILITATS",
              el7: "Aquests son els meus coneixements, però mai deixo d'apendre!",
              el8: "LLENGUATGES",
              el9: "EINES",
              el10: "ELS MEUS PROJECTES",
              el11: "Aquests son alguns dels projectes que he fet",
              el12: "¿VOLS QUE TREBALLEM JUNTS?",
              el13: "Direcció",
              el14: "Xarxes socials",
              el15: "Nom",
              el16: "Missatge",
              el17: "Enviar",
            },
          ],
        },
      ],
      selectedSection: 0,
      socialMedia: [
        {
          id: "0",
          name: "icons",
          elements: [
            {
              id: "0",
              name: "Github",
              image: require("../assets/githubMedia.png"),
              link: "https://github.com/ogonzalezz",
            },
            {
              id: "1",
              name: "Linkedin",
              image: require("../assets/linkedinMedia.png"),
              link: "https://www.linkedin.com/in/oscar-gonz%C3%A1lez-590474222/",
            },
            {
              id: "2",
              name: "Instagram",
              image: require("../assets/instaMedia.png"),
              link: "https://www.instagram.com/el_zarrias/",
            },
          ],
        },
      ],
      sections: [
        {
          id: "0",
          name: "LANGUAGES",
          image: require("../assets/prog.png"),
          elements: [
            {
              id: "0",
              name: "HTML5",
              image: require("../assets/html5.png"),
            },
            {
              id: "1",
              name: "CSS3",
              image: require("../assets/css3.png"),
            },
            {
              id: "2",
              name: "JAVASCRIPT",
              image: require("../assets/javascript.png"),
            },
            {
              id: "3",
              name: "PHP",
              image: require("../assets/php.png"),
            },
            {
              id: "4",
              name: "JAVA",
              image: require("../assets/java.png"),
            },
            {
              id: "5",
              name: "C++",
              image: require("../assets/c++.png"),
            },
          ],
        },
        {
          id: "1",
          name: "FRAMEWORKS",
          image: require("../assets/framework.png"),
          elements: [
            {
              id: "0",
              name: "VUE",
              image: require("../assets/vue.png"),
            },
            {
              id: "1",
              name: "REACT",
              image: require("../assets/react.png"),
            },
            {
              id: "2",
              name: "BOOTSTRAP",
              image: require("../assets/bootstrap.png"),
            },
            {
              id: "3",
              name: "SQL",
              image: require("../assets/sql.png"),
            },
            {
              id: "4",
              name: "LARAVEL",
              image: require("../assets/laravel.png"),
            },
            {
              id: "5",
              name: "SASS",
              image: require("../assets/sass.png"),
            },
          ],
        },
        {
          id: "2",
          name: "TOOLS",
          image: require("../assets/tool.png"),
          elements: [
            {
              id: "0",
              name: "Visual Studio Code",
              image: require("../assets/vscode.png"),
            },
            {
              id: "1",
              name: "MYSQL",
              image: require("../assets/mysql.png"),
            },
            {
              id: "2",
              name: "NETBEANS",
              image: require("../assets/netbeans.png"),
            },
            {
              id: "3",
              name: "Git",
              image: require("../assets/git.png"),
            },
            {
              id: "4",
              name: "GitHub",
              image: require("../assets/github.png"),
            },
            {
              id: "5",
              name: "Trello",
              image: require("../assets/trello.png"),
            },
          ],
        },
      ],
    };
  },
  methods: {
    changeSection(index) {
      this.selectedSection = index;
      console.log(index);
    },
  },
};
</script>

<style lang="scss" scoped>
@media only screen and (min-width: 768px) {
  .row1 {
    height: 90vh;
    margin: 0;
  }
  .row2 {
    height: 100vh;
  }
  .row3 {
    height: 100vh;
  }
  .row4 {
    height: 100vh;
  }
  .row5 {
    height: 100vh;
  }
  h1 {
    background-image: url(../assets/text.gif);
    -webkit-text-stroke: 2px #e68a6e; /* width and color */
    background-repeat: repeat;
    background-size: cover;
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    font-size: 130px;
    font-weight: bold;
    text-transform: uppercase;
    font-family: "Steelfish Rg", "helvetica neue", helvetica, arial, sans-serif;
    font-weight: 800;
    -webkit-font-smoothing: antialiased;
  }
  .cvButton {
    background-color: #ffc0ad;
    color: #271c19;
    width: 40%;
    height: 80px;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    font-weight: bold;
  }

  .gridItem {
    height: 60px;
    width: 60px;
    background-image: url("../assets/logo3.png");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    opacity: 0;
    transition: opacity 2s ease 0.4s, transform 0.8s ease;
    transform: scale(1);
  }
}
@media only screen and (max-width: 768px) {
  .row1 {
    height: 100vh;
    margin: 0;
  }
  .row2 {
    height: 100vh;
    padding: 0 35px;
  }
  .row3 {
    height: 100vh;
    padding: 0 35px;
  }
  .row4 {
    height: 100vh;
    padding: 0 35px;
  }
  .row5 {
    padding: 0 35px;
  }
  h1 {
    background-image: url(../assets/text.gif);
    -webkit-text-stroke: 1px #e68a6e; /* width and color */
    background-repeat: repeat;
    background-size: cover;
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    font-size: 45px;
    font-weight: bold;
    text-transform: uppercase;
    font-family: "Steelfish Rg", "helvetica neue", helvetica, arial, sans-serif;
    font-weight: 800;
    -webkit-font-smoothing: antialiased;
  }
  .palmtree {
    height: 70%;
    margin-top: 20px;
  }
  .cvButton {
    background-color: #ffc0ad;
    color: #271c19;
    width: 40%;
    height: 80px;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    font-weight: bold;
  }

  .gridItem {
    height: 30px;
    width: 30px;
    background-image: url("../assets/logo3.png");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    opacity: 0;
    transition: opacity 2s ease 0.4s, transform 0.8s ease;
    transform: scale(1);
  }
}
.before-enter {
  opacity: 0;
  transform: translateX(-100px);
  transition: all 2s ease-out;
  overflow-x: hidden;
}
.enter {
  opacity: 1;
  transform: translateX(0px);
}
.contactInfo {
  color: white;
}
.card-body {
  color: black;
}
.avatarImage {
  opacity: 0.8;
  border: 1px solid black;
  border-radius: 25px;
}
.cta {
  background-color: #ffc0ad;
  color: #271c19;
  width: 40%;
  height: 80px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
}
.cta:hover {
  background-color: #e68a6e;
}
.skillsButton {
  background-color: #ffc0ad;
  color: #271c19;
  width: 33%;
  height: 40px;
  justify-content: center;
  font-weight: bold;
}
.skillsButton:hover {
  background-color: #e68a6e;
}
hr {
  border: 0;
  height: 2px;
  background-image: linear-gradient(
    to right,
    transparent,
    #e68a6e,
    transparent
  );
}
.grid {
  display: flex;
  flex-wrap: wrap;
  width: 100%;
}

.gridItem:hover {
  opacity: 1;
  transition: opacity 0.2s ease;
  transform: scale(1.04);
}

.gridItem2 {
  position: absolute;
  top: 50%;
  left: 50%;
}

.card-body {
  background-color: #ffc0ad;
  border-radius: 20px;
}
</style>
