<template>
  <!--begin::Page loader-->
  <div class="page-loader flex-column">
    <span class="spinner-border text-primary" role="status"></span>
    <span class="text-muted fs-6 fw-bold mt-5">Loading...</span>
  </div>
  <!--end::Page Loader-->
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "doc-loader",
  components: {},
  props: {
    logo: String,
  },
});
</script>
