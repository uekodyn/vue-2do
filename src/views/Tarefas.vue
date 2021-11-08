<template>
<div>
  <v-col cols="12" >
      <v-text-field v-model="campoInput" label="Qual é a sua tarefa?"  outlined  clearable  @keyup.enter="handleAddTarefa">
      </v-text-field>
  </v-col>
    <lista-de-tarefas />
</div>
</template>

<script>
import ListaDeTarefas from '../components/tarefas/ListaDeTarefas.vue';

  export default {
    name: 'Home',
    components: {
        ListaDeTarefas
    },

    data(){
      return{
        campoInput: null,      
      }
    },
    created(){
      this.$store.commit('buscaTarefas');
    },
    methods:{
      handleAddTarefa(){
        // this.$store.commit('adicionaTarefa', this.campoInput)
        this.$store.dispatch('adicionaTarefa', this.campoInput)
        this.campoInput = null;
      }
    }
  }
  
</script>
