<template>
  <li :class="{clickable: clickable}">{{ label + ' ' +  something }}
    <!-- <button @click="onClick">click</button> -->
  </li>
</template>

<script>

export default {
  name: 'TListItem',
  props: ['label'],
  inject: ['clickable'],
  computed: {
    something () {
      return this.clickable ? 'yes' : 'no'
    }
  },
  // methods: {
  //   onClick () {
  //     this.clickable = true
  //   }
  // }
}

</script>

<style scoped>
li {
  padding: .35em .7em
}

.clickable {
  cursor: pointer;
  transition: background-color .5s linear
}
.clickable:hover {
  background: #efefef
}
</style>