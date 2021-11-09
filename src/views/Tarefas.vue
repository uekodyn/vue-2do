<template>
<div>
    <!-- <lista-de-tarefas /> -->
    <tab-semana />
    <div v-if="!$store.state.tarefas.length" class="bob-esponja animate__flip">
      <v-row class="mt-5" justify="center">
      <v-icon size="80" class="mt-9 animate__animated animate__flip " color="primary">mdi-check</v-icon>
      
      </v-row>
      <v-row class="justify-center">
      <span class="primary--text" >Nenhuma Tarefa</span>
      </v-row>
    </div>
</div>
</template>

<script>
// import ListaDeTarefas from '../components/tarefas/ListaDeTarefas.vue';
import TabSemana from '../components/tarefas/TabSemana.vue';

  export default {
    name: 'Home',
    components: {
        // ListaDeTarefas,
        TabSemana
    },
    created(){
      this.$store.commit('buscaTarefas');
    },
    mounted(){
      this.$store.commit('buscaTarefas');
    }

    
  }
  
</script>
<style scoped>
.bob-esponja {
  animation-duration: 5s;
  animation-delay: 5s;
  animation-iteration-count: 3;
}
</style>