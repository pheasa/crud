<script setup>
  import {RouterView} from 'vue-router';
  import Theader from "./components/HeaderPage.vue";
</script>
<template>
  <Theader v-if="TheaderStatus == true"/>
  <RouterView  @header="receiveDataFromChild"/>
</template>

<script>
export default {
  data(){
    return {
      testing:'pheakpheasa',
      TheaderStatus:false
    }
  },
  methods:{
    receiveDataFromChild(data) {
      this.TheaderStatus = data;
    }
  }
}
</script>

<style scoped>
.router-link-active.router-link-exact-active.nav-link {
  color: black;
}
</style>
