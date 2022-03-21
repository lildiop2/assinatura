<template>
  <div id="app">
    <!-- App.vue -->

<v-app>

  <v-app-bar app>
    <!-- -->
    <Header></Header>
    
  </v-app-bar>

  <!-- Sizes your content based upon application components -->
  <v-main>

    <!-- Provides the application the proper gutter -->
    <v-container fluid class=" d-flex">
 <v-card
 min-width="550"
 class="mx-auto"
  >
    <v-toolbar
      flat
      color="gray"
    >
      <v-icon>mdi-account</v-icon>
      <v-toolbar-title class="font-weight-light">
       Funcionario
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
  
        small
        @click="isEditing = !isEditing"
        
      >
      
      <h4 v-if="isEditing" class="ml-4">
        fechar
      </h4>
      <h4 v-else class="ml-4">
        editar
      </h4>
        <v-icon
          dark
          right
        >
          mdi-cancel
        </v-icon>
      </v-btn>
    </v-toolbar>
    <v-card-text>
      <v-text-field
        :disabled="!isEditing"
        color="dark"
        label="Nome"
        outlined
        v-model="nome"
      ></v-text-field>

       <v-text-field
        :disabled="!isEditing"
        color="dark"
        label="Funcao"
        outlined
        v-model="funcao"
      ></v-text-field>

          <v-select
          :disabled="!isEditing"
          v-model="select"
          :items="items"
          label="Empresa"
         outlined
         required
        ></v-select>
     
    </v-card-text>
    <v-divider></v-divider>
    <v-card-actions>
      <v-spacer></v-spacer>
      <v-btn
        :disabled="!isEditing"
        color="success"
        @click="save"
      >
        Salvar
      </v-btn>
    </v-card-actions>
    <v-snackbar
      v-model="hasSaved"
      :timeout="2000"
      absolute
      bottom
      left
    >
     Assinatura foi modificada!
    </v-snackbar>
  </v-card>

     <v-card  max-width="550"
          class="mx-auto my-4">
      <Assinatura :nome="nome" :funcao="funcao" :site="link_site" :logo="logo_empresa" :email="email" :link_email="link_email" :endereco="endereco" :link_endereco="link_endereco" :telephone="telephone" :link_telephone="link_telephone" :facebook="facebook" :linkedin="linkedin" :instagram="instagram" :youtube="youtube" ></Assinatura>  
     </v-card>
  
    </v-container>
  </v-main>

  <v-footer app>
    <!-- -->
  </v-footer>
</v-app>
  
  </div>
</template>

<script>
import Assinatura from './components/Assinatura.vue'
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    Assinatura,
    Header
  },
  data: () =>{
  return {
    nome: "Fulano de Tal",
    funcao: "Funcao Exercida",
    logo_empresa:"../assets/logo_voice_manager.png",
    link_site:"https://voicemanager.cloud/",
     telephone:"String",
      email:"String",
      endereco: "String",
      link_endereco: "String",
      facebook:"String",
      linkedin: "String",
      instagram: "String",
      youtube:"String",
     hasSaved: false,
        isEditing: null,
        select: null,
      items: [
        'Metodo',
        'Voice Manager'
      ],
    }
  },
  methods:{
    save () {
        this.isEditing = !this.isEditing
        this.hasSaved = true
        if(this.select==="Voice Manager"){
            this.logo_empresa="https://media-exp1.licdn.com/dms/image/C4D0BAQFfCDHi9S_dyA/company-logo_200_200/0/1647884157419?e=1655942400&v=beta&t=cOeOowwmUfYGZHLWYZ9lYQOaGPcyNxTiyYOaTu96Qt0",
            this.link_site="https://voicemanager.cloud/",
            this.telephone="0800 580 5811",
            this.link_telephone="tel:0800 580 5811",
            this.email="contato@voicemanager.cloud",
            this.link_email="mailto:atendimento@metodotelecom.com.br",
            this.endereco="Av. das Nações Unidas, n° 12.995 - 10 andar - Cidade Monções, São Paulo - SP, 04578-000",
            this.link_endereco="https://goo.gl/maps/AouhvHFfFh8GfoUU6",
            this.facebook="https://www.facebook.com/voicemanagercloud",
            this.linkedin="https://br.linkedin.com/company/voice-manager",
            this.instagram="https://www.instagram.com/voice_manager/",
            this.youtube="https://www.youtube.com/c/VoiceManager/videos"
        }else{
           this.logo_empresa="https://media-exp1.licdn.com/dms/image/C4D0BAQHXdfvHPgp7qg/company-logo_200_200/0/1610112149514?e=1655942400&v=beta&t=4FFTHMRRbH1Kbz8Rn66gmDHowMpdiGM42-dasuAwFSE",
            this.link_site="https://metodotelecom.com.br/",
            this.telephone="(31) 2102-1100",
            this.link_telephone="tel:+553121021100",
            this.link_email="mailto:atendimento@metodotelecom.com.br",
            this.email="atendimento@metodotelecom.com.br",
            this.endereco=" Av. Barão Homem de Melo, 3382, 1° andar, Estoril, Belo Horizonte/MG",
            this.link_endereco="https://goo.gl/maps/DaJ9pZQGK1PPjvNh8",
            this.facebook="https://www.facebook.com/metodotelecom/",
            this.linkedin="https://www.linkedin.com/company/metodo-telecomunicacoes/",
            this.instagram="https://instagram.com/metodotelecom",
            this.youtube="https://www.youtube.com/channel/UCCSl775QesXJ0CiJcRyLxaA"

        }
        console.log(this.logo_empresa +"===>"+ this.link_site)
      },
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
