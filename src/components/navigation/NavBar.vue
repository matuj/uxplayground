<script setup lang="ts">
import { defineProps, withDefaults } from "vue";

interface Props {
  msg: string;
  visible?: boolean;
}

withDefaults(defineProps<Props>(), { msg: "Hi" });
</script>

<template>
  <header class="w-full text-sm" :visible="visible">
    <div class="fixed top-0 left-0 w-full h-16 bg-white">
      <div
        class="flex flex-nowrap h-full px-8 mx-auto border-b border-solid border-gray-200"
      >
        {{ msg }}
      </div>
    </div>
  </header>
</template>
