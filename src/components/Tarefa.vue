<template>

    <Box>
        <div class="columns">
            <div class="column is-7">

                {{ tarefa.descricao || 'Tarefa sem descrição'}}

            </div>

        </div>
        <div class="column">
            <Cronometro :tempoEmSegundos="tarefa.duracaoEmSegundos" />
        </div>

    </Box>
   

</template>


<script lang="ts">

import Itarefa from '@/Interfaces/ITarefa';
import { defineComponent, PropType } from 'vue'
import Cronometro from './Cronometro.vue'
import Box from './Box.vue'



export default defineComponent({
    name: 'Tarefa-vue',
    components: {
    Cronometro,
    Box
},
    props: {
        tarefa: {
            type: Object as PropType<Itarefa>,
            required: true
        }
    }
})

</script>


<style scoped>
.box {
    background: #FAF0CA;
}
</style>