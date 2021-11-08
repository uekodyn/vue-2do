<template>
  <div>
    <drop-list :items="tarefasComputadas" @reorder="$event.apply(tarefasComputadas)">
            <template v-slot:item="{item, reorder}">
                <drag :key="item.id" :data="item" >
                    <!-- <v-list-item>
                        <v-list-item-avatar>
                            <v-img :src="item.avatar"/>
                        </v-list-item-avatar>
                        <v-list-item-content>
                            <v-list-item-title v-html="item.titulo"/>
                            <v-list-item-subtitle v-html="item.subtitle"/>
                        </v-list-item-content>
                    </v-list-item> -->
                    <tarefa :tarefa="item" style="background-color: white"  :style="reorder ? {borderLeft: '2px solid #1976D2', marginLeft:'-2px'} : {}"/>
                    <v-divider/>
                </drag>
            </template>
        </drop-list>
  </div>

</template>

<script>
import {Drag,DropList} from "vue-easy-dnd";
import Tarefa from './Tarefa.vue';

    export default {
        name: "App",
        components: {
            Drag,
            DropList,
            Tarefa
        },
        computed:{
            tarefasComputadas(){
                return this.$store.state.tarefas;
            }
        }

    }
</script>

<style>

</style>