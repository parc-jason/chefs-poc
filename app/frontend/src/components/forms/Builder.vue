<template>
  <FormBuilder
    :form="{ display: 'form' }"
    :options="{}"
    @change="onChangeMethod"
  />
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
    },
  }
};
</script>
