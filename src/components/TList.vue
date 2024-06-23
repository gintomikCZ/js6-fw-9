<template>
  <ul>
    <TListItem v-for="item in items" :label="item"/>
  </ul>
</template>

<script>
import TListItem from '@/components/TListItem.vue'
export default {
  name: 'TList',
  props: ['items'],
  components: { TListItem }
}


</script>