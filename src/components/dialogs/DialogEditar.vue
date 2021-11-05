<template>
  <div class="text-center">
    <v-dialog
      v-model="dialog"
      width="290"
    >
      <!-- <template v-slot:activator="{ on, attrs }">
        <v-btn
          color="red lighten-2"
          dark
          v-bind="attrs"
          v-on="on"
        >
          Click Me
        </v-btn>
      </template> -->

      <v-card>
        <v-card-title class="text-h5 grey lighten-2">
          Editar
        </v-card-title>

        <v-card-text class="mt-3">
         Informe o novo titulo.
        </v-card-text>
        <v-text-field v-model="campoInput" label="Título" class="mx-3" outlined >
        </v-text-field>

        <v-divider></v-divider>

        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="red darken-1"
            text
            @click="dialog = false"
          >
            Cancelar
          </v-btn>
          <v-btn
            color="primary"
            text
            @click="dialog = false"
          >
            Editar
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </div>
</template>

<script>
export default {

}
</script>
<script>
  export default {
    data () {
      return {
        dialog: false,
      }
    },
  }
</script>

<style>

</style>