<template>
  <div>
    <link
      rel="stylesheet"
      href="https://stackpath.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css"
    />
    <link
      rel="stylesheet"
      href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css"
    />
    <link rel="stylesheet" href="https://unpkg.com/formiojs@latest/dist/formio.full.min.css" />
    <FormBuilder :form="{ display: 'form' }" :options="{}" @change="onChangeMethod" />
  </div>
</template>

<script>
import { FormBuilder } from 'vue-formio';

export default {
  name: 'FormTwo',
  components: {
    FormBuilder
  },
  methods: {
    onChangeMethod(schema) {
      console.debug('schema', schema); // eslint-disable-line no-console
    }
  }
};
</script>
