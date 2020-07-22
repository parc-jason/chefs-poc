<template>
  <v-container>
    <BaseSecure>
      <h1 class="my-6 text-center">Form Three</h1>
      <FormThree />
    </BaseSecure>
  </v-container>
</template>

<script>
import FormThree from '@/components/forms/FormThree.vue';

export default {
  name: 'FormThreeView',
  components: {
    FormThree
  }
};
</script>
