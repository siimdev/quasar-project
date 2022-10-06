<template>
  <div class="q-pa-md">
    <TopSide></TopSide>

    <div class="q-col-gutter-md row items-start">
      <div class="col-6">
        <LeftSide></LeftSide>
      </div>

      <div class="col-6">
        <RightSide></RightSide>
      </div>
    </div>
  </div>

  <q-page-sticky position="bottom-right" :offset="[18, 18]">
    <q-btn
      align="around"
      class="btn-fixed-width"
      size="lg"
      icon="fa-solid fa-scale-unbalanced"
      color="accent"
      label="Weight now!"
    />
  </q-page-sticky>
</template>

<script>
import { defineComponent } from "vue";
import RightSide from "../components/rightSide.vue";
import LeftSide from "../components/leftSide.vue";
import TopSide from "src/components/topSide.vue";

export default defineComponent({
  name: "IndexPage",
  components: { RightSide, LeftSide, TopSide },
});
</script>
