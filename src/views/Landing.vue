<template>
  <div class="wrapper">
    <parallax class="section page-header header-filter" :style="headerStyle">
      <div class="container">
        <div class="md-layout">
          <div
            class="md-layout-item md-size-50 md-small-size-70 md-xsmall-size-100"
          >
            <!-- <h1 class="title">Faça seu cadastro/pré-cadastro.</h1> -->
            <!-- <h4>
              TextoTextoTextoTextoTextoTextoTextoTextoTextoTexto
              TextoTextoTextoTextoTextoTextoTextoTextoTextoTexto
              TextoTextoTextoTextoTextoTextoTextoTextoTextoTexto TextoTextoTexto
            </h4> -->
            <br />
          </div>
        </div>
      </div>
    </parallax>
    <div class="main main-raised">
      <div class="section">
        <div class="container"></div>
      </div>
      <div class="section section-contacts">
        <div class="container">
          <div class="md-layout">
            <div class="md-layout-item md-size-66 md-xsmall-size-100 mx-auto">
              <h1 class="text-center title">Fale conosco</h1>
              <h4 class="text-center description">
                
              </h4>

              <!-- inicio do formulário -->
              <form class="contact-form" @submit="checkForm" @submit.prevent="sendEmail" type="reset">
                <!-- <p class="alert" v-if="successo.length">
                  <span class="closebtn" onclick="this.parentElement.style.display='none';">&times;</span> 
                  <strong>Alerta!</strong> Seu orçamento foi enviado com sucesso!
                </p> -->
                <p v-if="errors.length">
                  <b>Por favor, corrija o(s) seguinte(s) erro(s):</b>
                  <ul>
                    <li v-for="error in errors" :key="error.id">
                      {{ error }}
                    </li>
                  </ul>
                </p>

                

                <div class="md-layout">
                  <div class="md-layout-item md-size-50">
                    <md-field>
                      <label>Seu nome </label>
                      <md-input
                        v-model="name"
                        required=""
                        id="name"
                        name="name"
                        type="text"
                      ></md-input>
                    </md-field>
                  </div>
                  <!-- arquiteto -->
                  <div class="md-layout-item md-size-50">
                    <md-field>
                      <label >Arquiteto</label>
                      <md-input v-model="arquiteto" name="arquiteto" type="text"></md-input>
                    </md-field>
                  </div>
                </div>
                <!-- email -->
                <div class="md-layout">
                  <div class="md-layout-item md-size-50">
                    <md-field maxlength="5">
                      <label>Seu email </label>
                      <md-input v-model="email" required="" name="email" type="email"></md-input>
                    </md-field>
                  </div>
                  <!-- numero -->
                  <div class="md-layout-item md-size-50">
                    <md-field maxlength="5">
                      <label>Número para contato (DDD + número) </label>
                      <md-input
                        v-model="fone"
                        name="fone"
                        required=""
                        type="text"
                        v-mask="'55+ (##)#####-####'"
                      ></md-input>
                    </md-field>
                  </div>
                </div>
                <!-- endereço -->
                <div class="md-layout">
                  <div class="md-layout-item md-size-50">
                    <md-field>
                      <label>Logradouro </label>
                      <md-input v-model="endereco" required="" name="endereco" type="text"></md-input>
                    </md-field>
                  </div>
                  <!-- bairro -->
                  <div class="md-layout-item md-size-50">
                    <md-field>
                      <label>Bairro </label>
                      <md-input
                        v-model="bairro"
                        name="bairro"
                        required=""
                        type="text"
                      ></md-input>
                    </md-field>
                  </div>
                </div>
                <div class="md-layout">
                  <!-- cidade -->
                  <div class="md-layout-item md-size-50">
                    <md-field>
                      <label>Cidade </label>
                      <md-input v-model="cidade" required="" name="cidade" type="text"></md-input>
                    </md-field>
                  </div>
                  <!-- complemento -->
                  <div class="md-layout-item md-size-50">
                    <md-field maxlength="5">
                      <label>Complemento </label>
                      <md-input
                        v-model="compl"
                        name="compl"
                        type="text"
                      ></md-input>
                    </md-field>
                  </div>
                </div>
                <div class="md-layout">
                  <div class="md-layout-item md-size-50">
                    <br />
                    <label>Tipo de serviço</label>
                    <br />
                    <div id="example-3">
                      <input
                        type="checkbox"
                        id="auditiva"
                        value="Paisagismo de interiores"
                        v-model="servico"
                        name="servico"
                      />
                      <label for="john">Paisagismo de interiores</label>
                      <br />
                      <input
                        type="checkbox"
                        id="Paisagismo de jardim externo"
                        value="Paisagismo de jardim externo"
                        v-model="servico"
                        name="servico"
                      />
                      <label for="mike">Paisagismo de jardim externo</label>
                      <br />
                      <input
                        type="checkbox"
                        id="visual"
                        value="Assessoria"
                        v-model="servico"
                        name="servico"
                      />
                      <label for="Assessoria">Assessoria</label>
                      <br />
                      <!-- <md-checkbox
                        type="checkbox"
                        id="multipla"
                        value="Manutenção de jardins"
                        v-model="deficiency"
                      />
                      <label for="mike">Manutenção de jardins</label>
                      <br /> -->
                      <input
                        class="check"
                        type="checkbox"
                        id="Projeto"
                        value="Projeto"
                        v-model="servico"
                        name="servico"
                      />
                      <label for="Projeto">Projeto</label>
                      <br />
                      <!-- <span>Nomes assinalados: {{ name }}</span> -->
                    </div>
                  </div>
                </div>
                
                <br />
                <div class="md-layout">
                  <div class="md-layout-item md-size-33 mx-auto text-center">
                    <!-- <md-input type="submit" value="enviar"></md-input> -->
                    <md-button class="md-success" type="submit" v-on:click="submit" value="Send"
                      >Enviar cadastro</md-button
                    >
                    <input type="reset" value="Limpar">
                  </div>
                </div>
                <!-- <span>
                  fone: {{ fone }}
                  <br />
                </span> -->
              </form>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import emailjs from 'emailjs-com';

export default {
  bodyClass: "landing-page",
  props: {
    header: {
      type: String,
      default: require("@/assets/img/capa.png")
    },
    teamImg1: {
      type: String,
      default: require("@/assets/img/faces/avatar.jpg")
    },
    teamImg2: {
      type: String,
      default: require("@/assets/img/faces/christian.jpg")
    },
    teamImg3: {
      type: String,
      default: require("@/assets/img/faces/kendall.jpg")
    }
  },
  data() {
    return {
      errors: [],
      name: '',
      arquiteto:'',
      email: '',
      endereco: '',
      bairro: '',
      cidade:'',
      compl:'',
      fone: '',
      servico: [],
      sucesso: 'false'
    };
  },
  computed: {
    headerStyle() {
      return {
        backgroundImage: `url(${this.header})`
      };
    }
  },
  methods: {
    checkForm: function(e) {
      if (this.name && this.fone && this.email) {
        return true;
      }
      this.errors = [];
      if (!this.name) {
        this.errors.push("O nome é obrigatório.");
      }
      if (!this.fone) {
        this.errors.push("Seu telefone é obrigatório.");
      }
      if (!this.email) {
        this.errors.push("Seu email é obrigatório.");
      }
      // if (!this.contact) {
      //   this.errors.push("Seu contato é obrigatório.");
      // }
      // if (!this.date) {
      //   this.errors.push("A data de nascimento é obrigatória.");
      // }
      // if (!this.CPF) {
      //   this.errors.push("CPF é obrigatório.");
      // }
      // if (!this.nationality) {
      //   this.errors.push("Sua nacionalidade é obrigatória.");
      // }
      // if (!this.doc) {
      //   this.errors.push("Seu documento de identificação é obrigatório.");
      // }
      // if (!this.sex) {
      //   this.errors.push("Informe o seu sexo");
      // }
      
      
      
      
      e.preventDefault();
    },
    submit: function (event) {
      if (!this.name ){
        alert('Por favor, preencha todos os dados obrigatórios')
      }
      // alert('Olá ' + this.name + '!')
      // // `event` é o evento DOM nativo
      // if (event) {
      //   alert(event.target.tagName)
      // }
    },
    sendEmail: (e) => {
      emailjs.sendForm('service_mtcmigw', 'template_byg01t2', e.target, 'user_36dq2VofQoBRwAvAnGVKJ')
        .then((result) => {
            console.log('SUCCESSO!', result.status, result.text);
            alert('Seu orçamento foi enviado com sucesso!')
            $("input").name("")
        }, (error) => {
            console.log('FAILED...', error);
      });
    
      e.preventDefault();
    }
  }
};
</script>

<style lang="scss" scoped>
.md-card-actions.text-center {
  display: flex;
  justify-content: center !important;
}
.contact-form {
  margin-top: 30px;
}
.md-has-textarea + .md-layout {
  margin-top: 15px;
}
.alert {
  padding: 20px;
  background-color: #008000;
  color: white;
}

.closebtn {
  margin-left: 15px;
  color: white;
  font-weight: bold;
  float: right;
  font-size: 22px;
  line-height: 20px;
  cursor: pointer;
  transition: 0.3s;
}

.closebtn:hover {
  color: black;
}

</style>