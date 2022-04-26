<template>
  <div class="q-pa-md">
    <div class="q-gutter-y-md" style="max-width: 600px">
      <q-card>
        <q-tabs
          v-model="tab"
          dense
          class="text-grey"
          active-color="primary"
          indicator-color="primary"
          align="justify"
          narrow-indicator
        >
          <q-tab name="all" label="All" />
          <q-tab name="launches" label="Launched" />
          <q-tab name="upcoming" label="Upcoming" />
        </q-tabs>

        <q-separator />

        <q-tab-panels v-model="tab" animated style="background: gray">
          <q-tab-panel name="all">
            <div class="text-h6 my-2" style="background: white">
              <div class="row" style="text-align: center">
                <div class="col-4">aa</div>
                <div class="col-4">aa</div>
                <div class="col-4">aa</div>
              </div>
            </div>
          </q-tab-panel>

          <q-tab-panel name="launches">
            <div class="text-h6" style="background: white">
              <div class="row" style="text-align: center">
                <div class="col-4">bb</div>
                <div class="col-4">bb</div>
                <div class="col-4">bb</div>
              </div>
            </div>
          </q-tab-panel>

          <q-tab-panel name="upcoming">
            <div class="text-h6" style="background: white">
              <div class="row" style="text-align: center">
                <div class="col-4">cc</div>
                <div class="col-4">cc</div>
                <div class="col-4">cc</div>
              </div>
            </div>
          </q-tab-panel>
        </q-tab-panels>
      </q-card>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue';
export default {
  setup() {
    const data = async () => {
      await api.get('https://api.spacexdata.com/v4/launches/latest');
    };
    console.log(data.value);
    return {
      tab: ref('all'),
    };
  },
};
</script>
