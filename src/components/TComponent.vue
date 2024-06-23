<template>

<div>this is my component</div>
<button @click="onClick">click me</button>

</template>

<script>

export default {
  name: 'TComponent',
  mounted () {
    console.log(this.injectedData)
  },
  methods: {
    onClick () {
      console.log(this.$root.parentData)
      this.$parent.onChildClick()
    }
  },
  inject: ['injectedData']
}

</script>