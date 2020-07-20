<template>
  <v-container>
    <h1 class="my-6 text-center">Form</h1>
    <formio
      src="https://chefs-jujaga-wxpbtr-dev.pathfinder.gov.bc.ca/bcgov-common/bcgovcommonfeedback"
      v-on:submit="onSubmitMethod"
    />
  </v-container>
</template>

<script>
import { Form } from 'vue-formio';

export default {
  name: 'Form',
  components: {
    formio: Form
  },
  methods: {
    onSubmitMethod(submission) {
      console.log(submission); // eslint-disable-line no-console
    }
  }
};
</script>
