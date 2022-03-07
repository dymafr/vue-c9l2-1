<template>
  <input
    type="text"
    :value="prenom"
    @input="$emit('update:prenom', $event.target.value)"
  />
  <input
    type="text"
    :value="nom"
    @input="$emit('update:nom', $event.target.value)"
  />
</template>

<script setup lang="ts">
defineProps<{
  prenom: string;
  nom: string;
}>();

defineEmits<{
  (e: 'update:prenom', value: string);
  (e: 'update:nom', value: string);
}>();
</script>

<style scoped lang="scss"></style>
