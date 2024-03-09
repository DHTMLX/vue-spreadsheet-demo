<script>
import { Spreadsheet } from "@dhx/trial-spreadsheet";
import "@dhx/trial-spreadsheet/codebase/spreadsheet.min.css";

export default {
  props: ["data"],
  data() {
    return {
      spreadsheet: null,
    };
  },

  mounted() {
    this.spreadsheet = new Spreadsheet(this.$refs.cont, {});
    this.spreadsheet.parse(this.data);
  },
  unmounted() {
    this.spreadsheet.destructor();
    this.$refs.cont.innerHTML = "";
  },
};
</script>

<template>
  <div ref="cont" style="width: 100%; height: 100%"></div>
</template>
