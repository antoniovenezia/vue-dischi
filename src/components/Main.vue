<template>
  <div>{{ dischi }}</div>
</template>

<script>
import axios from 'axios';

export default {
name: "Main",

data() {
        return{
            dischi: [],
        }
    },
    created() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((result) => {
            this.dischi = result.data.response
            console.log(this.dischi)
        });
    },

    
}
</script>


<style lang="scss" scoped>
.main {
  background-color: #1e2d3b;
  height: 500px;
}
</style>