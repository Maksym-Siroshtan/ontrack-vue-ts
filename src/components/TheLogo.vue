<script setup>
import { currentPage, navigate } from '../router'
import { scrollToCurrentHour } from '../timeline-items'
import { PAGE_TIMELINE } from '../constants'
import { ICON_CLOCK } from '../icons'
import BaseIcon from './BaseIcon.vue'

function handleClick() {
  currentPage.value === PAGE_TIMELINE ? scrollToCurrentHour(true) : navigate(PAGE_TIMELINE)
}
</script>

<template>
  <a :href="`#${PAGE_TIMELINE}`" @click="handleClick" class="bg-black text-white p-1 rounded scale-125 origin-left">
    <BaseIcon :name="ICON_CLOCK" class="h-5" />
  </a>
</template>
