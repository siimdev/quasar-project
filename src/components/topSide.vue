<template>
  <div class="q-pa-md">
    <q-banner
      class="bg-primary text-white q-p-none q-m-none h1 text-center shadow-2"
    >
      <div class="text-h5">
        Base: {{ base.age }}, {{ base.region }} and {{ base.gender }}
      </div>
    </q-banner>
  </div>
</template>

<script>
const example = ["abc"];
import { ref } from "vue";
export default {
  setup() {
    return {
      example,
      base: ref({
        age: "18-74",
        region: "County",
        gender: "All",
      }),
    };
  },
};
</script>
