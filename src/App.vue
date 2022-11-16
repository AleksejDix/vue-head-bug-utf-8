<template>Broken utf8</template>

<script setup lang="ts">
import { useHead } from "@vueuse/head";

const str = "hello 123";

useHead({
  htmlAttrs: {
    lang: "en", // Change to your language
  },
  meta: [
    { charset: "utf-8" },
    { name: "viewport", content: "width=device-width, initial-scale=1" },
  ],
});
console.log(
  /^[a-zA-ZÀ-ÖØ-öø-ÿĄąĆćČčĎďĘęĚěŁłŃńŇňŘřŚśŠšŤťŮůŹźŻŽžż]+$/g.test(str)
);
</script>
