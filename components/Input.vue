<template>
    <div class="grid grid-cols-3 items-center">
        <label for="input" class="text-primary font-bold">{{ props.label }}</label>
        <input v-model="props.value" :type="props.type" :placeholder="props.placeholder" class="border border-primary bg-secondary text-background col-span-2 rounded-md p-2" />
    </div>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  label: String,
  type: String,
  placeholder: String,
  value: String,
});
</script>