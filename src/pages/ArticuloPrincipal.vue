<template>
  <div>
    <div class="row">
      <q-select dense class="col-7" v-model="ordenarPor" outlined
      :options="opcionesOrdenar" label="Ordenar Por "/>
    </div>
    <div class=" q-pa-md row items-start q-gutter-md ">
        <q-card class="my-card col-6 col-md-3 q-ma-none" v-for="(item, key) in 9" :key="key">
          <img class="q-pa-md" src="https://cdn.quasar.dev/img/mountains.jpg">

          <q-card-section>
            <div class="text-h6">Our Changing Planet</div>
            <div class="text-subtitle2">by John Doe</div>
          </q-card-section>

          <q-separator />

          <q-card-actions align="right">
            <q-btn color="green">VER DETALLES</q-btn>
          </q-card-actions>
        </q-card>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const ordenarPor = ref('Precio')
const opcionesOrdenar = ref(['Precio', 'Fecha'])

</script>
