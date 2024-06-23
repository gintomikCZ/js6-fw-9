<template>
  <!-- <div>
    <h2>teleport</h2>
    <div>
      <TModal @clicked="onClicked"/>
    </div>
    <TComponent />
  </div> -->
  <TList :items="listItems" />

</template>

<script>
// import TModal from '@/components/TModal.vue'
// import TComponent from '@/components/TComponent.vue'
import TList from '@/components/TList.vue'
export default {
  name: 'App',
  data () {
    return {
      listItems: ['jablko', 'hruška', 'švestka'],
      listIsClickable: false
    }
  },
  provide () {
    return {
      clickable: this.listIsClickable
    }
  },
  components: { TList }
  // data () {
  //   return {
  //     parentData: 'ahoj .... '
  //   }
  // },
  // provide () {
  //   return {
  //     injectedData: 'i am injected dependency'
  //   }
  // },
  // methods: {
  //   onClicked () {
  //     console.log('clicked')
  //   },
  //   onChildClick () {
  //     console.log('child clicked')
  //   }
  // },

}




</script>

<style scoped>

</style>