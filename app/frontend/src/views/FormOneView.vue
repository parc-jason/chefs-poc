<template>
  <v-container>
    <h1 class="my-6 text-center">Form One</h1>
    <FormOne />
  </v-container>
</template>

<script>
import FormOne from '@/components/forms/FormOne.vue';

export default {
  name: 'FormOneView',
  components: {
    FormOne
  }
};
</script>
