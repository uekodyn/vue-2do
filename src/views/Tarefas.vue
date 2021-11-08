<template>
<div>
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

    
    created(){
      this.$store.commit('buscaTarefas');
    },
    
  }
  
</script>
