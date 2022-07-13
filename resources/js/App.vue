<template>
  <div>HOME VUE</div>
</template>

<script>
export default {
    name: 'App',

    data(){
        return {
            postApi: 'http://127.0.0.1:8000/api/index'
        }
    },

    methods:{
        getApi(){
            axios.get(this.postApi)
            .then(res => {
                console.log(res.data)
            })
        }
    },

    mounted(){
        return this.getApi();
    }
}
</script>

<style>

</style>