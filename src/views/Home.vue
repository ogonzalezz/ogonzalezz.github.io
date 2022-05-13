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
              <div class="gridItem2">?</div>
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
      <b-col>
        <b-button class="cta" href="#contactSection">GET IN TOUCH</b-button>
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
      >
        <b-col v-scrollanimation>
          <div class="text-left">
            <h2 class="pb-4">
              <img src="../assets/dado1.svg" alt="" height="55vh" /> ABOUT ME
            </h2>
            <p>
              Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dolores
              porro ad eum, tenetur perferendis molestiae incidunt. Maxime
              consectetur deserunt qui molestiae impedit facilis, quod eum
              consequatur consequuntur autem nostrum dolore.
            </p>
            <b-button class="cvButton" href="./avatar.png" download
              >GET MY CV</b-button
            >
            <!-- <a href="./avatar.png" download>
            <button type="button">Download</button>
          </a> -->
          </div>
        </b-col>
        <b-col v-scrollanimation>
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
      >
        <b-col v-scrollanimation>
          <div class="text-left">
            <h2 class="pb-4">
              <img src="../assets/dado2.svg" alt="" height="55vh" /> MY SKILLS
            </h2>
            <p>
              Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dolores
              porro ad eum, tenetur perferendis molestiae incidunt. Maxime
              consectetur deserunt qui molestiae impedit facilis, quod eum
              consequatur consequuntur autem nostrum dolore.
            </p>
            <b-button
              class="me-2 skillsButton"
              v-for="(section, index) in sections"
              :key="section.name"
              @click="changeSection(index)"
            >
              {{ section.name }}
            </b-button>
            <!-- <a href="./avatar.png" download>
            <button type="button">Download</button>
          </a> -->
          </div>
        </b-col>
        <b-col v-scrollanimation>
          <div>
            <b-container class="bv-example-row">
              <b-row>
                <b-col
                  cols="4"
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
                    <img :src="element.image" alt="" width="100%" />
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
      >
        <b-col v-scrollanimation>
          <div class="text-left">
            <h2 class="pb-4">
              <img src="../assets/dado3.svg" alt="" height="55vh" /> MY PROJECTS
            </h2>
            <p>
              Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dolores
              porro ad eum, tenetur perferendis molestiae incidunt. Maxime
              consectetur deserunt qui molestiae impedit facilis, quod eum
              consequatur consequuntur autem nostrum dolore.
            </p>
          </div>
        </b-col>
        <b-col v-scrollanimation>
          <div>
            <b-carousel
              id="carousel-fade"
              style="text-shadow: 0px 0px 2px #000"
              fade
              indicators
              img-width="1024"
              img-height="480"
            >
              <a
                href="https://github.com/OscarCastellaSanSegundo/Project2"
                target="_blank"
              >
                <b-carousel-slide
                  caption="JS GAME"
                  img-src="https://picsum.photos/1024/480/?image=10"
                ></b-carousel-slide>
              </a>
              <a
                href="https://github.com/OscarCastellaSanSegundo/Project2"
                target="_blank"
              >
                <b-carousel-slide
                  caption="HEALTH APP"
                  img-src="https://picsum.photos/1024/480/?image=10"
                ></b-carousel-slide>
              </a>
              <a
                href="https://github.com/OscarCastellaSanSegundo/Project2"
                target="_blank"
              >
                <b-carousel-slide
                  caption="MOVIE APP"
                  img-src="https://picsum.photos/1024/480/?image=10"
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
      >
        <b-col class="text-left">
          <div>
            <h2 class="text-center">
              <img src="../assets/logo2.svg" alt="" height="55vh" />Do you want
              to work together?
            </h2>
          </div>
          <div class="mt-4">
            <h3>Address</h3>
            <p>Montcada i Reixac, Barcelona</p>
          </div>
          <div>
            <h3>Phone</h3>
            <p>727735532</p>
          </div>
          <div>
            <h3>Email</h3>
            <p>opt3.oscar@gmail.com</p>
          </div>
        </b-col>
        <b-col align-h="center">
          <b-card style="max-width: 20rem" class="mx-auto mb-2">
            <div class="mt-2">Name</div>
            <b-form-input placeholder="e.g. John Doe"></b-form-input>
            <div class="mt-2">Email</div>
            <b-form-input placeholder="Enter your name"></b-form-input>
            <div class="mt-2">Message</div>
            <b-form-textarea
              id="textarea"
              placeholder="Enter something..."
              rows="3"
              max-rows="6"
            ></b-form-textarea>
            <b-button href="#" variant="primary" class="mt-2">Send</b-button>
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
  components: {
    /* "skills-card": SkillsCard, */
    /* "cube-3d": Cube3d, */
    /* "footer-landing": FooterLanding, */
  },
  data() {
    return {
      selectedSection: 0,
      sections: [
        {
          id: "0",
          name: "LANGUAGES",
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
    height: 100vh;
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
    font-size: 35px;
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
    height: 40px;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    font-weight: bold;
  }
}
.before-enter {
  opacity: 0;
  transform: translateX(100px);
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
</style>
