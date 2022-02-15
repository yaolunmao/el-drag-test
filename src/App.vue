<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import draggable from "./lib/vuedrag/src/vuedraggable";
import { ref } from "vue";
const test_list = ref([{ name: 'ElColorPicker' }, { name: 'ElInput' }, { name: 'ElButton' }]);
</script>

<template>
  <draggable :group="'group'" :list="test_list" item-key="nam1e">
    <template #item="{ element }">
      <component :is="element.name"></component>
    </template>
  </draggable>
</template>


