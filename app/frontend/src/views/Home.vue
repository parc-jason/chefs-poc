<template>
  <v-container>
    <h1 class="my-6 text-center">Form Builder</h1>
    <Builder />
  </v-container>
</template>

<script>
import Builder from '@/components/forms/Builder.vue';

export default {
  name: 'Home',
  components: {
    Builder
  }
};
</script>
