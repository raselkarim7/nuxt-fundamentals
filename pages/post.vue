<template>
    <div class="container border">

         <article>
            <h2>pages/post.vue</h2> 
            <h3 class="title">Remember this</h3>
            <ul>
                <li>
                    When you want to use an element that will be present in all pages, 
                    Like the navbar or sidebar, The "layout" is the place to put in.
                    <ul>
                        <li>
                            1. At layouts/default.vue the  nuxt component will render the contents
                            of the active page.
                        </li>
                        <li>
                            To add navbar on top, we can place it in here. See at "default.vue"
                        </li>

                    </ul>
                </li>
                <li>
                    aaaaaaaa
                </li>
               <li>
                    aaaaaaaa
                </li>
                <li>
                    aaaaaaaa
                </li>
            </ul>
        </article>
    </div>
</template>

<script>
export default {

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
