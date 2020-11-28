<template>
  <button @click="incremento">
    Contagem é: {{ count }}, o Dobro é {{ double }}, Click para incrementar!
  </button>
</template>


<script>
/**
 * A composition API expões propriedades de
 * componentes como Funções, então a primeira etapa
 * é importar as funções que precisamos
 */

import { ref, computed } from 'vue'


/**
 * Metodo SETUP(){}
 * Função que retorna propriedades e funções para o template
 * 
 */
export default {
  setup(){

    /**
     * Declaramos um propriedade reativa chamada Count usando a função ref
     * Ela pode encapsular qualquer valor ou objeto e retorna-lo como uma propriedade.
     * O valor passado será mantido na propriedade value da ref criada
     * 
     */
    const count = ref(0)

    /**
     * Se quiser acessar o valor da constante count é preciso utilizar
     * propriedade value.
     * É o que fazemos na computed double para calcular o dobro.
     */
    const double = computed(() => count.value * 2)

    /**
     * dentro do setup(){} podemos declarar funções sem a necessidade 
     * de chamar o methods: {}
     */
    function incremento(){
      count.value++
    }
    
    /**
     * E por fim. Retornamos os dados que o template poderá usar.
     */
    return {
      count, double, incremento
    }
  }
}

</script>