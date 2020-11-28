<template>
  <button @click="incremento()">
    Contagem é: {{ count }}, o Dobro é {{ double }}, Click para incrementar!
  </button>
</template>


<script>
export default {
  data(){
    return{
      count: 0,
    }
  },

computed: {
  double(){
    return this.count * 2
  }
},

  methods: {
    incremento(){
      this.count++
    }
  }
}

</script>