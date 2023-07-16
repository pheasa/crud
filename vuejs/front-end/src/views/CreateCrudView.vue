<script setup>
import createCrud from '../components/CreateRow.vue';
</script>
<template>
    <createCrud v-bind="{field:field}"/>
</template>

<script>
export default {
    beforeMount(){
        this.$emit('header', true)
    },
    data(){
        return {
            field : [
                'name',
                'email'
            ]
        }
    }
}
</script>