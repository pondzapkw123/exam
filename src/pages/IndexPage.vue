<template>
  <q-page class="row items-center justify-evenly">
    <Example-component />
  </q-page>
</template>

<script lang="ts">
import ExampleComponent from 'components/ExampleComponent.vue';
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'IndexPage',
  components: { ExampleComponent },
  setup() {
    return {};
  },
});
</script>
