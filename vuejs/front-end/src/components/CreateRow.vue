<script setup>
import { capitalize } from 'vue';
import axios from 'axios';
</script>
<template>
    <div class="container">
        <div class="container-fluid">
            <h1>Create</h1>
            <div class="form-floating mb-3" v-for="value in field" v-bind:key="value">
                <input type="text" class="form-control" id="{{ value }}" placeholder="Type your name here!">
                <label for="{{ value }}">{{ capitalize(value) }}</label>
            </div>
            <button type="button" class="btn btn-success float-end" @click="validateData">Okay</button>
        </div>
    </div>
</template>
<script>
export default {
    props:['field'],
    mounted(){
        
    },
    methods:{
        validateData(){
            axios.get().then();
        }
    }
}
</script>