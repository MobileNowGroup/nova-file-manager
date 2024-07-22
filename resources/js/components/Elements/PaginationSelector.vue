<script setup lang="ts">
import range from 'lodash/range'
import Select from '@/components/Elements/Select.vue'
import { onBeforeMount } from 'vue'

interface Props {
  perPage: number
  perPageOptions: number[]
  setPerPage: (perPage: number) => void
}

withDefaults(defineProps<Props>(), {
  perPage: 15
})
</script>

<template>
  <Select :current="perPage" :on-click="setPerPage" :options="perPageOptions" />
</template>
