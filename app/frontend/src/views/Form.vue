<template>
  <v-container>
    <h1 class="my-6 text-center">Form</h1>
    <FormOne />
  </v-container>
</template>

<script>
import FormOne from '@/components/forms/FormOne.vue';

export default {
  name: 'Form',
  components: {
    FormOne
  }
};
</script>
