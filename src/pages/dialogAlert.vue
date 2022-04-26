<template>
  <div class="q-pa-md q-gutter-sm">
    <q-dialog v-model="props.alert">
      <q-card>
        <q-card-section>
          <div class="text-h6">Alert</div>
        </q-card-section>

        <q-card-section class="q-pt-none"> test </q-card-section>

        <q-card-actions align="right">
          <q-btn flat label="OK" color="primary" v-close-popup />
        </q-card-actions>
      </q-card>
    </q-dialog>
  </div>
</template>

<script lang="ts">
export default {
  props: {
    alert: {
      type: Boolean,
      default: false,
    },
  },
};
</script>
