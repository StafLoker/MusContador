<template lang="pug">
v-row
  span {{ header }}
v-row
  v-btn.reduce(
    icon="mdi-menu-left"
    variant="text"
    @click="reduce"
  )
  v-col
    v-card(
      variant="outlined"
    ) {{ value }}
  v-btn.increase(
    icon="mdi-menu-right"
    variant="text"
    @click="increase"
  )
</template>

<script lang="ts" setup>
defineProps({
  header: { type: String, required: true },
  value: { type: Number, required: true }
})

function increase() {
  this.value++
}

function reduce() {
  this.value--
}
</script>

<style>
.reduce{
  color: red
}

.increase{
  color: green
}
</style>
