<template lang="pug">
v-app
  v-main
    v-container
      v-row.justify-center
        h1 MusContador
      v-row
        v-col
          FieldPoint(
            header="A",
            :value="0"
          )
        v-col
          FieldPoint(
            header="B",
            :value="0"
          )
      v-row
        v-col
          FieldPoint(
            header="Grande",
            :value="0"
          )
        v-col
          FieldPoint(
            header="Chicas",
            :value="0"
          )
        v-col
          FieldPoint(
            header="Pares",
            :value="0"
          )
        v-col
          FieldPoint(
            header="Juego",
            :value="0"
          )
      v-row
        v-col
          v-btn A
        v-col
          v-btn B
      v-row
        v-btn Reiniciar
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
//
</script>
