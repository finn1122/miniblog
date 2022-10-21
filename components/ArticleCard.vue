<template>
    <div class="article-card">
         <NuxtLink :to="slug"><h3>{{ title }}</h3></NuxtLink>
        <div class="author">
        <p>Por {{ author }}</p>
        <small>Fecha de publicacion: {{ date }}</small>
        <figure>
            <img :src="cover" alt="cover">
        </figure>
        <p>{{ description }}</p>
        <div class="actions">
            <NuxtLink class="btn" :to="slug">Ir al post</NuxtLink>
            
        </div>
        </div>
    </div>
   
</template>

<script>
export default {
    name: 'ArticleCard',
    props: {
        slug: {
            type: String,
            default: '',

        },
        title: {
            type: String,
            default: '',

        },
        author: {
            type: String,
            default: '',

        },
        date: {
            type: String,
            default: '',

        },
        cover: {
            type: String,
            default: '',

        },
        description: {
            type: String,
            default: '',

        },
    }
}
</script>

<style lang="scss">
.article-card {
    @apply border border-red-700;
}
</style>