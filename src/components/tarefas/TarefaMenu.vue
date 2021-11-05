<template>
  <div>
    <v-menu offset-y>
      <template v-slot:activator="{ on, attrs }">
        <v-btn  color="primary"   dark  v-bind="attrs"  v-on="on"   icon >
            <v-icon >
                mdi-dots-vertical
            </v-icon>
        </v-btn>
      </template>
      <v-list>
        <v-list-item  v-for="(item, index) in items"  :key="index" @click="item.click()">
            <v-icon>
                {{item.icone}}
            </v-icon>
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
    <dialog-editar />
  </div>
</template>


<script>
import DialogEditar from '../dialogs/DialogEditar.vue'


  export default {
  components: { DialogEditar },
    data: () => ({
      items: [
        { 
            icone:"mdi-pencil",  
            title: 'Editar',
            click(){
               
            }
        },

        {   
            icone:"mdi-trash-can",
            title: 'Excluir' },
            
           
            
      ],
    }),
  }
</script>

<style>

</style>