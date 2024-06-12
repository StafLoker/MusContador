<template lang="pug">
v-app
  v-main
    v-container
      v-row.justify-center
        h1 Contador de Mus
      v-row
        v-col
          FieldPoint(
            header="A"
            :value="parentValue"
            @update:value="handleValueUpdate"
          )
        v-col
          FieldPoint(
            header="B"
            :value="parentValue"
            @update:value="handleValueUpdate"
          )
      v-row
        v-col
          FieldPoint(
            header="Grande"
            :value="parentValue"
            @update:value="handleValueUpdate"
          )
        v-col
          FieldPoint(
            header="Chicas"
            :value="parentValue"
            @update:value="handleValueUpdate"
          )
        v-col
          FieldPoint(
            header="Pares"
            :value="parentValue"
            @update:value="handleValueUpdate"
          )
        v-col
          FieldPoint(
            header="Juego"
            :value="parentValue"
            @update:value="handleValueUpdate"
          )
      v-row
        v-col
          v-btn A
        v-col
          v-btn B
      v-row.justify-end
        v-btn(
          @click="parentValue = 0"
        ) Reiniciar
    v-footer
      span MusContador
      v-spacer
      span 2024
      v-spacer
      a(
        href="https://github.com/StafLoker/MusContador"
        target="_blank"
      )
        v-icon(
          icon="mdi-github"
        )
</template>

<script lang="ts" setup>
import { ref } from 'vue';

const parentValue = ref(0);

function handleValueUpdate(newValue: number) {
  parentValue.value = newValue;
}
</script>
