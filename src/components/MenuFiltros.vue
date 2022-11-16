<template>
<div class="q-pa-md" style="max-width: 350px, , height: 20px;">
  <h6 class="q-mb-none">Marca</h6>
    <q-list bordered separator>
      <q-item  v-for="(marca, key) in marcas" :key="'mar-'+key" clickable v-ripple>
        <q-item-section>
          <q-checkbox v-model="marca.value" color="green">
            {{marca.label}}<q-badge class="q-ml-sm" color="green" align="top">{{marca.cantidad}}</q-badge>
          </q-checkbox>
        </q-item-section>
      </q-item>
    </q-list>
    <h6 class="q-my-none">Sistemas</h6>
    <q-list bordered separator>
      <q-item  v-for="(sistema, key) in sistemas" :key="'sis-'+key" clickable v-ripple>
        <q-item-section>
          <q-checkbox v-model="sistema.value" color="green">
            {{sistema.label}}<q-badge class="q-ml-sm" color="green" align="top">{{sistema.cantidad}}</q-badge>
          </q-checkbox>
        </q-item-section>
      </q-item>
    </q-list>
    <h6 class="q-my-none">Pantallas</h6>
    <q-list bordered separator>
      <q-item  v-for="(pantalla, key) in pantallas" :key="'pant-'+key" clickable v-ripple>
        <q-item-section>
          <q-checkbox v-model="pantalla.value" color="green">
            {{pantalla.label}}<q-badge class="q-ml-sm" color="green" align="top">{{pantalla.cantidad}}</q-badge>
          </q-checkbox>
        </q-item-section>
      </q-item>
    </q-list>
  </div>
</template>

<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'MenuFiltros',
  setup () {
    return {
      marcas: ref([
        { value: false, label: 'Samsung', cantidad: 25 },
        { value: false, label: 'Huawei', cantidad: 20 },
        { value: false, label: 'Nokia', cantidad: 4 },
        { value: false, label: 'iPhone', cantidad: 5 },
        { value: false, label: 'Xiomi', cantidad: 2 }
      ]),
      sistemas: ref([
        { value: false, label: 'Android', cantidad: 24 },
        { value: false, label: 'Windows', cantidad: 19 },
        { value: false, label: 'Ios', cantidad: 8 }
      ]),
      pantallas: ref([
        { value: false, label: '6.0"', cantidad: 4 },
        { value: false, label: '5.5"', cantidad: 9 },
        { value: false, label: '5,0"', cantidad: 2 }
      ])
    }
  }
})
</script>
