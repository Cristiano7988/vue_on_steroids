<template>
    <div>
        <Header />
        <section class="about-page">
            <h1>About Us</h1>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ipsa, ipsam eius. Suscipit nesciunt dolorum debitis explicabo qui facilis voluptate ipsum? Vel aperiam corporis asperiores saepe ut est optio eveniet et. Lorem ipsum, dolor sit amet consectetur adipisicing elit. Obcaecati tenetur iste, eum minima quis officiis reprehenderit ratione suscipit corporis, beatae neque quas? Deleniti animi accusamus repellendus optio nobis alias maxime.</p>
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Sit magnam dignissimos id qui minus dicta non mollitia odio magni. Facilis qui, obcaecati ipsum culpa omnis quisquam quas fugit doloribus vel. Lorem ipsum dolor sit, amet consectetur adipisicing elit. Nihil nulla possimus beatae aperiam consequuntur, explicabo quis earum perspiciatis, sed tenetur obcaecati dolorum minima dolores cumque corporis sint! Voluptatem, eveniet rem.</p>
        </section>
    </div>
</template>

<script>
import Header from "~/components/Header.vue"

export default {
    components: { Header }
}
</script>

<style scoped>
    .about-page {
        text-align: center;
        padding: 0 10%;
        margin: auto;
    }
</style>