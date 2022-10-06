<template>
  <div class="q-gutter-lg q-pa-md">
    <div class="text-h5 text-weight-bold">ABC12345 DP/PM - NO</div>
    <q-list bordered>
      <q-item clickable v-ripple>
        <q-item-section>Completes</q-item-section>
        <q-item-section avatar>
          <q-badge color="accent" class="text-h5"> 50</q-badge>
        </q-item-section>
      </q-item>

      <q-item clickable v-ripple>
        <q-item-section>Screened</q-item-section>
        <q-badge color="grey" class="text-h5"> 10</q-badge>
      </q-item>

      <q-item clickable v-ripple>
        <q-item-section>Quotafull</q-item-section>
        <q-badge color="grey" class="text-h5"> 5</q-badge>
      </q-item>

      <q-item clickable v-ripple>
        <q-item-section>Partial</q-item-section>
        <q-badge color="grey" class="text-h5"> 7</q-badge>
      </q-item>

      <q-separator />

      <q-item clickable v-ripple>
        <q-item-section>IR</q-item-section>
        <q-item-section avatar> 90% </q-item-section>
      </q-item>
    </q-list>

    <q-card>
      <div class="q-pa-md">
        <q-range
          v-model="ageModel"
          :min="15"
          :max="110"
          :left-label-value="'Age: ' + ageModel.min"
          :right-label-value="'Age: ' + ageModel.max"
          label-always
        />
      </div>
    </q-card>

    <q-card>
      <q-card-section>
        <q-select
          v-model="regionSelected"
          :options="[
            { label: 'Landsdel', value: 'landstel' },
            { label: 'Nuts2', value: 'nust2' },
            { label: 'Region', value: 'region' },
          ]"
          label="Region"
        />

        <div class="q-mt-sm">
          <q-chip clickable color="grey" text-color="white">Region1</q-chip>
          <q-chip clickable color="grey" text-color="white">Region2</q-chip>
          <q-chip clickable color="grey" text-color="white">Region3</q-chip>
          <q-chip clickable color="grey" text-color="white">Region4</q-chip>
        </div>
      </q-card-section>
    </q-card>

    <q-card>
      <q-card-section>
        <q-btn-toggle
          v-model="model"
          toggle-color="primary"
          :options="[
            { label: 'Male', value: 'male' },
            { label: 'Female', value: 'female' },
            { label: 'Both', value: 'both' },
          ]"
        />
      </q-card-section>
    </q-card>

    <!-- <div class="q-gutter-md" style="max-width: 300px">
      <q-input v-model="text" label="Standard" />

      <q-input filled v-model="text" label="Filled" />

      <q-input outlined v-model="text" label="Outlined" />

      <q-input standout v-model="text" label="Standout" />
    </div> -->

    <!-- <div class="cursor-pointer" style="width: 100px">
          Click me
          <q-popup-edit
            v-model="label"
            class="bg-accent text-white"
            v-slot="scope"
          >
            <q-input
              dark
              color="white"
              v-model="scope.value"
              dense
              autofocus
              counter
              @keyup.enter="scope.set"
            >
              <template v-slot:append>
                <q-icon name="edit" />
              </template>
            </q-input>
          </q-popup-edit>
        </div> -->
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    return {
      text: ref(""),
      model: ref("both"),
      regionSelected: ref("region"),
      ageModel: ref({
        min: 18,
        max: 74,
      }),
    };
  },
};
</script>
