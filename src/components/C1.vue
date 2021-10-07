<template>
  <div>
    C1:
    <div>{{ $t("hello", { world: $t("world") }) }}</div>
    <i18n-t keypath="hello" tag="div">
      <template #world>
        <strong>{{ $t("world") }}</strong>
      </template>
    </i18n-t>

    <br />

    <C2>
      <div>{{ $t("hello", { world: $t("world") }) }}</div>
      <i18n-t keypath="hello" tag="div">
        <template #world>
          <strong>{{ $t("world") }}</strong>
        </template>
      </i18n-t>

      <C3>
      <div>{{ $t("hello", { world: $t("world") }) }}</div>
      <i18n-t keypath="hello" tag="div">
        <template #world>
          <strong>{{ $t("world") }}</strong>
        </template>
      </i18n-t>
      </C3>
    </C2>
  </div>
</template>

<script>
import C2 from "./C2";
import C3 from "./C3";

export default {
  components: {
    C2,
    C3,
  },
  i18n: {
    messages: {
      en: {
        hello: "Hello {world}",
        world: "world!",
      },
    },
  },
};
</script>
