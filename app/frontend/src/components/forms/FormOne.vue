<template>
  <Formio
    :form="formUrl"
    :src="source"
    :submission="submission"
    v-on:change="onChangeMethod"
    v-on:submit="onSubmitMethod"
  />
</template>

<script>
import { Form } from 'vue-formio';

export default {
  name: 'FormEmbed',
  components: {
    Formio: Form
  },
  data: () => ({
    form: {},
    formUrl:
      'https://chefs-jujaga-wxpbtr-dev.pathfinder.gov.bc.ca/bcgov-common/formone',
    submission: {
      data: {
        feedbackOnFormIoTool: 'test'
      }
    }
  }),
  methods: {
    onChangeMethod(change) {
      const changed = change.changed;
      console.debug('change', changed); // eslint-disable-line no-console
      if (changed) {
        this.submission.data[changed.instance.path] = changed.value;
      }
    },
    onSubmitMethod(submission) {
      console.debug('submit', submission); // eslint-disable-line no-console
    }
  }
};
</script>
