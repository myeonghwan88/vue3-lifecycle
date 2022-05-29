<template>
  <h1>{{ count }}</h1>
</template>

<script>
export default {
  data(){
    return{
      count: 2
    }
  },
  beforeCreate() {
    console.log('Befor Create!', this.count) // Befor Create! undefined
  },
  created() {
    console.log('Created!', this.count) // Created! 2
  },
  beforeMount() {
    console.log('Befor Mounte!') // Befor Mounte!
    console.log(document.querySelector('h1')) // null
  },
  mounted() {
    console.log('Mounted!') // Mounted!
    console.log(document.querySelector('h1')) // <h1>2</h1>
  }
}
</script>