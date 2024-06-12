<template lang="pug">
v-row.justify-center
  span {{ props.header }}
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
import { defineProps, defineEmits, ref, watch } from "vue"

const props = defineProps<{
  header: string
  value: number
}>()

const emit = defineEmits<{
  (e: "update:value", value: number): void
}>()

const localValue = ref(props.value)

watch(
  () => props.value,
  newVal => {
    localValue.value = newVal
  }
)

function increase() {
  localValue.value++
  emit("update:value", localValue.value)
}

function reduce() {
  localValue.value--
  emit("update:value", localValue.value)
}
</script>

<style>
.reduce {
  color: rgb(228, 36, 36);
}

.increase {
  color: rgb(31, 225, 31);
}
</style>
