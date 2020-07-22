<template>
  <Formio
    :form="form"
    :src="formUrl"
    :submission="submission"
    @change="onChangeMethod"
    @submit="onSubmitMethod"
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
        formOneTextArea: 'prefilled value'
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
