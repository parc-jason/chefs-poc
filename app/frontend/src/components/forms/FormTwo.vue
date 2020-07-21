<template>
  <v-container>
    <BaseSecure>
      <h2>Secure Form (Form2)</h2>
      <formio :src="formUrl" v-on:submit="onSubmitMethod" />
    </BaseSecure>
  </v-container>
</template>

<script>
import { Form } from 'vue-formio';

export default {
  name: 'FormTwo',
  components: {
    formio: Form
  },
  data: () => ({
    // Load these from vuex or some other state store system.
    formUrl: 'https://chefs-jujaga-wxpbtr-dev.pathfinder.gov.bc.ca/bcgov-common/formtwo',
  }),
  methods: {
    onSubmitMethod(submission) {
      console.log(submission); // eslint-disable-line no-console
    }
  }
};
</script>
