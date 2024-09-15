<script>
import { Spreadsheet } from "@dhx/trial-spreadsheet";
import "@dhx/trial-spreadsheet/codebase/spreadsheet.min.css";

export default {
  props: ["data"],

  mounted() {
    this.spreadsheet = new Spreadsheet(this.$refs.container, {});
    this.spreadsheet.parse(this.data);
  },
  unmounted() {
    this.spreadsheet.destructor();
  }
};
</script>

<template>
  <div ref="container" class="widget"></div>
</template>
