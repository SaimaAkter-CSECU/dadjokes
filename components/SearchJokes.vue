<template>
    <div>
        <form @submit.prevent="OnSubmit">
            <input type="text" v-model="text" placeholder="Search Jokes...">
            <input type="submit" value="Seach jokes"> 
        </form>
    </div>
</template>

<script>
    export default {
        name: 'SearchJokes',
        data(){
            return{
                text: ''
            }
        },
        methods:{
            OnSubmit(){
                this.$emit("search-text", this.text); 
                this.text = ''; 
            }
        }
    }
</script>