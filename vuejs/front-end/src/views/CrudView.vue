<script setup>
import dataTable from '../components/DataTable.vue';
import { RouterLink } from 'vue-router';
</script>

<template>
    <div class="container">
        <div class="container-fluid">
          <RouterLink to="/crud-create">
            <button type="button" class="btn btn-primary float-end">Create</button>
          </RouterLink>
        </div>
        <div class="container-fluid">
            <dataTable v-bind="{tbheader:tbheader,data:data,action:action}"/>
        </div>
    </div>
</template>

<script>
export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: "crud",
    props: [],
    data() {
        return {
            tbheader: ["Id", "Nmae", "Email", "Action"],
            data: [
                { id: "1", name: "pheak pheasa", email: "Pheasa92@gmail.com" },
                { id: "2", name: "pheak pheasa", email: "Pheasa92@gmail.com" }
            ],
            action: [{ "Edit": "btn btn-success", "Delete": "btn btn-danger" }],
            pheasa: "pheakpheasa"
        };
    },
    beforeMount() {
        // console.log(this)
        // enable display header
        this.$emit("header", true);
    },
    mounted() {
        // this.testing();
    },
    method: {},
    components: { RouterLink }
}
</script>
