<template>
  <!--begin::Card-->
  <div class="card">
    <!--begin::Card Body-->
    <div class="card-body fs-6 py-15 px-10 py-lg-15 px-lg-15 text-gray-700">
      <!--begin::Section-->
      <div class="pt-5">
        <!--begin::Heading-->
        <h1 class="anchor fw-bolder mb-5" id="quick_setup">
          <router-link to="#quick_setup"></router-link>
          Quick Setup
        </h1>
        <!--end::Heading-->

        <!--begin::Block-->
        <div class="pt-4">
          Metronic 8 supports full <b>Dark Mode</b> that you can easily setup
          following the below instructions.
        </div>
        <!--end::Block-->

        <ol class="pt-4">
          <li>
            In file <code>demo1/src/App.vue</code> replace main scss files to
            dark mode.
            <CodeHighlighter lang="scss">{{
              `
@import "assets/sass/plugins.dark";
@import "assets/sass/style.dark";
`
            }}</CodeHighlighter>
          </li>
          <li>
            In file <code>demo1/public/index.html</code> add dark-mode class
            name to the <code>&lt;body&gt;</code> tag.
            <CodeHighlighter lang="html">{{ htmlCode }}</CodeHighlighter>
          </li>
        </ol>
      </div>
      <!--end::Section-->
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, onMounted } from "vue";
import { setCurrentPageBreadcrumbs } from "@/core/helpers/breadcrumb";
import CodeHighlighter from "@/components/highlighters/CodeHighlighter.vue";

export default defineComponent({
  name: "dark-mode",
  components: {
    CodeHighlighter,
  },
  setup() {
    onMounted(() => {
      setCurrentPageBreadcrumbs("Dark mode", ["Getting Started"]);
    });

    const htmlCode = `<body class="dark-mode">`;

    return {
      htmlCode,
    };
  },
});
</script>
