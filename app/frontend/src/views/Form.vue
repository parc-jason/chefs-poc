<template>
  <v-container>
    <h1 class="my-6 text-center">Form</h1>
    <FormEmbed />
  </v-container>
</template>

<script>
import FormEmbed from '@/components/FormEmbed.vue';

export default {
  name: 'Form',
  components: {
    FormEmbed
  }
};
</script>
