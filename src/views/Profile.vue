<template>
  <div class="wrapper">
    <parallax
      class="section page-header header-filter"
      :style="headerStyle"
    ></parallax>
    <div class="main main-raised">
      <div class="section profile-content">
        <div class="container">
          <div class="md-layout">
            <div class="md-layout-item md-size-50 mx-auto">
              <div class="profile">
                <div class="avatar">
                  <img
                    :src="img1"
                    alt="Circle Image"
                    class="img-raised rounded-circle img-fluid"
                  />
                </div>
                <div class="name">
                  <h3 class="title">Carlos Nascimento</h3>
                  <h6>Engenheiro de software e front-end</h6>
                  <md-button
                    href="https://www.linkedin.com/in/carlos-nascimento-7a9a681a3/"
                    class="md-just-icon md-simple md-linkedin"
                    ><i class="fab fa-linkedin"></i
                  ></md-button>
                  <md-button
                    href="https://github.com/carlosag16"
                    class="md-just-icon md-simple md-github"
                    ><i class="fab fa-github"></i
                  ></md-button>
                  <!-- <md-button
                    href="javascript:void(0)"
                    class="md-just-icon md-simple md-facebook"
                    ><i class="fab fa-facebook"></i
                  ></md-button> -->
                </div>
              </div>
              <div class="description text-center">
                <p>
                  Desenolvedor web e formando em engenharia da computação, busco
                  me atualizar nas principais tecnologia do mercado. Possuo
                  bastante experiência no desevolvimento front-end de diversos
                  site, tal como o site
                  <a href="http://bc.ufpa.br/">da Biblioteca Central da UFPA</a>
                </p>
              </div>
            </div>
            <div class="md-layout-item md-size-50 mx-auto">
              <div class="profile">
                <div class="avatar">
                  <img
                    :src="img2"
                    alt="Circle Image"
                    class="img-raised rounded-circle img-fluid"
                  />
                </div>
                <div class="name">
                  <h3 class="title">Samantha Silva</h3>
                  <h6>Desenvolvedora Full-stack</h6>
                  <md-button
                    href="https://www.linkedin.com/in/samantha-silva-860a82109/"
                    class="md-just-icon md-simple md-linkedin"
                    ><i class="fab fa-linkedin"></i
                  ></md-button>
                  <md-button
                    href="https://github.com/CylonSam "
                    class="md-just-icon md-simple md-github"
                    ><i class="fab fa-github"></i
                  ></md-button>
                  <!-- <md-button
                    href="javascript:void(0)"
                    class="md-just-icon md-simple md-facebook"
                    ><i class="fab fa-facebook"></i
                  ></md-button> -->
                </div>
              </div>
              <div class="description text-center">
                <p>
                  Entusiasta de Python, Node.js e hot dogs. Atualmente
                  aprendendo Vue.js e cursando Engenharia da Computação na UFPA.
                </p>
              </div>
            </div>
          </div>
          <!-- <div class="profile-tabs">
            <tabs
              :tab-name="['Studio', 'Work', 'Favorite']"
              :tab-icon="['camera', 'palette', 'favorite']"
              plain
              nav-pills-icons
              color-button="success"
            >
              here you can add your content for tab-content 
              <template slot="tab-pane-1">
                <div class="md-layout">
                  <div class="md-layout-item md-size-25 ml-auto">
                    <img :src="tabPane1[0].image" class="rounded" />
                    <img :src="tabPane1[1].image" class="rounded" />
                  </div>
                  <div class="md-layout-item md-size-25 mr-auto">
                    <img :src="tabPane1[3].image" class="rounded" />
                    <img :src="tabPane1[2].image" class="rounded" />
                  </div>
                </div>
              </template>
              <template slot="tab-pane-2">
                <div class="md-layout">
                  <div class="md-layout-item md-size-25 ml-auto">
                    <img :src="tabPane2[0].image" class="rounded" />
                    <img :src="tabPane2[1].image" class="rounded" />
                    <img :src="tabPane2[2].image" class="rounded" />
                  </div>
                  <div class="md-layout-item md-size-25 mr-auto">
                    <img :src="tabPane2[3].image" class="rounded" />
                    <img :src="tabPane2[4].image" class="rounded" />
                  </div>
                </div>
              </template>
              <template slot="tab-pane-3">
                <div class="md-layout">
                  <div class="md-layout-item md-size-25 ml-auto">
                    <img :src="tabPane3[0].image" class="rounded" />
                    <img :src="tabPane3[1].image" class="rounded" />
                  </div>
                  <div class="md-layout-item md-size-25 mr-auto">
                    <img :src="tabPane3[2].image" class="rounded" />
                    <img :src="tabPane3[3].image" class="rounded" />
                    <img :src="tabPane3[4].image" class="rounded" />
                  </div>
                </div>
              </template>
            </tabs>
          </div> -->
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { Tabs } from "@/components";
export default {
  components: {},
  bodyClass: "profile-page",
  data() {
    return {
      tabPane1: [
        { image: require("@/assets/img/examples/studio-1.jpg") },
        { image: require("@/assets/img/examples/studio-2.jpg") },
        { image: require("@/assets/img/examples/studio-4.jpg") },
        { image: require("@/assets/img/examples/studio-5.jpg") }
      ],
      tabPane2: [
        { image: require("@/assets/img/examples/olu-eletu.jpg") },
        { image: require("@/assets/img/examples/clem-onojeghuo.jpg") },
        { image: require("@/assets/img/examples/cynthia-del-rio.jpg") },
        { image: require("@/assets/img/examples/mariya-georgieva.jpg") },
        { image: require("@/assets/img/examples/clem-onojegaw.jpg") }
      ],
      tabPane3: [
        { image: require("@/assets/img/examples/mariya-georgieva.jpg") },
        { image: require("@/assets/img/examples/studio-3.jpg") },
        { image: require("@/assets/img/examples/clem-onojeghuo.jpg") },
        { image: require("@/assets/img/examples/olu-eletu.jpg") },
        { image: require("@/assets/img/examples/studio-1.jpg") }
      ]
    };
  },
  props: {
    header: {
      type: String,
      default: require("@/assets/img/city-profile.jpg")
    },
    img1: {
      type: String,
      default: require("@/assets/img/faces/carlos.jpeg")
    },
    img2: {
      type: String,
      default: require("@/assets/img/faces/samantha.jpeg")
    }
  },
  computed: {
    headerStyle() {
      return {
        backgroundImage: `url(${this.header})`
      };
    }
  }
};
</script>

<style lang="scss" scoped>
.section {
  padding: 0;
}

.profile-tabs::v-deep {
  .md-card-tabs .md-list {
    justify-content: center;
  }

  [class*="tab-pane-"] {
    margin-top: 3.213rem;
    padding-bottom: 50px;

    img {
      margin-bottom: 2.142rem;
    }
  }
}
</style>
