<template>
  <transition name="fade">
      <i18n-t keypath="hello" tag="p">
        <template #world>
            <b>{{ $t("world") }}</b>
        </template>
      </i18n-t>
  </transition>
</template>

<script>
export default {
  i18n: {
    messages: {
      en: {
        hello: "Hello {world}",
        world: "world!",
      },
    },
  }
};
</script>