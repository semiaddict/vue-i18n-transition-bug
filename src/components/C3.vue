<template>
  <div>C3 slot: <slot></slot></div>
</template>

<script>
export default {
  i18n: {
    messages: {
      en: {
        hello: "Hello {world} - C3",
        world: "world! - C3",
      },
    },
  },
};
</script>