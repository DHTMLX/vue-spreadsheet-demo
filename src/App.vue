<script>
import Spreadsheet from "./components/Spreadsheet.vue";
import { getData } from "./data";

export default {
  components: { Spreadsheet },
  data() {
    return { data: getData() };
  },
};
</script>

<template>
  <Spreadsheet :data="data" />
</template>
