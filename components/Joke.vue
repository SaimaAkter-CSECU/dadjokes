<template>
    <nuxt-link :to="'jokes/'+id">
        <div class="joke">
            <p>{{joke}}</p>
        </div>
    </nuxt-link>
</template>

<script>
    export default {
        name: 'Joke',
        props: ['joke', 'id']
    }
</script>

<style scoped>
    .joke{
        padding: 1rem; 
        border-bottom: 1px solid rgba(255,255,255,0.5);

    }
</style>