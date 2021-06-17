<template>

  <q-layout view="hHh lpR fFf">

    <q-header elevated class="bg-primary text-white">
      <q-toolbar>
        <q-btn dense flat round icon="menu" @click="left = !left" />

        <q-toolbar-title class="text-h4">
          <q-avatar>
            <img src="../assets/svg/study.svg"/>
          </q-avatar>
          Cursos
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-drawer show-if-above v-model="left" side="left" bordered>
       <q-list>
        <q-item-label
          header
          class="text-grey-8"
        >
          Essential Links
        </q-item-label>
        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>

    <q-footer class="text-white bg-footer">
      <q-toolbar>
         <p>
           Cursos - todos os direitos reservados copyright; 2021
          </p>
      </q-toolbar>
    </q-footer>
    </q-layout>


</template>

<style scoped>
  .bg-footer{
    background-color: #0d3b69;
  }
</style>

<script>
import EssentialLink from 'components/EssentialLink.vue'

const linksData = [
  {
    title: 'FICR',
    caption: 'Faculdade Católica Imaculada Sra Conceição',
    icon: 'school',
    link: 'https://ficr.catolica.edu.br'
  },
  {
    title: 'Formações',
    caption: 'Lista dos Cursos',
    icon: 'list',
    link: '/formacoes'
  },
   {
    title: 'Atividades',
    caption: 'Lista de Atividades',
    icon: 'list',
    link: '/atividade'
  },
  {
    title: 'Usuários',
    caption: 'Lista de Usuários',
    icon: 'account_circle',
    link: 'https://chat.quasar.dev'
  },
  
];

export default {
  name: 'MainLayout',
  components: { EssentialLink },
  data () {
    return {
      left: false,
      essentialLinks: linksData
    }
  }
}
</script>
