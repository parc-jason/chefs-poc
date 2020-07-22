<template>
  <v-container>
    <BaseSecure>
      <h1 class="my-6 text-center">Form Two</h1>
      <FormTwo />
    </BaseSecure>
  </v-container>
</template>

<script>
import FormTwo from '@/components/forms/FormTwo.vue';

export default {
  name: 'FormTwoView',
  components: {
    FormTwo
  }
};
</script>
