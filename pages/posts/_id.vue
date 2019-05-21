<template>
    <div class="container">

         <article class="border">
            <ul>
                <li>
                    <h1>Id: {{post.id}}</h1>
                </li>
               <li>
                    <h3>Title: {{post.title}}</h3>
                </li>
                <li>
                    Content: {{post.content}}
                </li>
            </ul>
        </article>
        <aside class=" m-0 p-1    ">
            <h3 >Related Posts</h3>
            <ul v-for="related in relatedPosts" :key="related.id">
                <nuxt-link :to="{name: 'posts-id', params: {id: related.id}}">
                    {{related.title}}
                </nuxt-link>
            </ul>
        </aside>
    </div>
</template>

<script>
export default {
    data() {
        return {
            id: this.$route.params.id,
        }
    },
    computed: {
        post() {
            return this.$store.state.posts.all.find(post => post.id === this.id)
        },
        relatedPosts() {
            return this.$store.state.posts.all.filter(post => post.id !== this.id)
        }
    }
}
</script>

<style>
.container {
    display: flex;
    justify-content: space-between;
    line-height: 1.5rem;
}
article * {
    margin-bottom: 1rem;
}
aside {
    min-width: 200px;
    max-width: 200px;
    padding-left: 2rem;
}
.title {
    font-size: 2rem;
} 

</style>
