<template>
    <section>
        <h2>Bunzo Template Features</h2>
        <div class="features-wrapper">
            <div class="feature" v-for=" feature, key in features" :key="key">
                <img :src="feature.image" :alt="feature.alt">
                <h3>{{ feature.caption }}</h3>
                <p>{{ feature.detials }}</p>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            features: [
                {
                    image: "./src/assets/images/nuxt.png",
                    alt: "Vue Nuxt JS",
                    caption: "Vue Nuxt JS",
                    detials: "Vue.js is a JavaScript framework that is widely popular because it is easy to use"
                },
                {
                    image: "./src/assets/images/wp.png",
                    alt: "WordPress (Headless)",
                    caption: "WordPress (Headless)",
                    detials: "The headless CMS approach provides more flexibility on the back-end"
                },
                {
                    image: "./src/assets/images/graphql.png",
                    alt: "GraphQL",
                    caption: "GraphQL",
                    detials: "GraphQL is a query language for APIs queries with your existing data"
                },
                {
                    image: "./src/assets/images/jamstack.png",
                    alt: "Jamstack",
                    caption: "Jamstack",
                    detials: "The modern way to build Websites and Apps that delivers better performance"
                },
                {
                    image: "./src/assets/images/tailwind.png",
                    alt: "Tailwind CSS",
                    caption: "Tailwind CSS",
                    detials: "Tailwind CSS is a utility-first CSS framework for rapidly building custom user interfaces."
                },
                {
                    image: "./src/assets/images/jquery.png",
                    alt: "No jQuery",
                    caption: "No jQuery",
                    detials: "No jQuery dependency used in the template for better performance"
                },
            ]
        }
    }
}
</script>

<style scoped>
section {
    padding: 100px 7%;
    text-align: center;
    color: #373737;
}

h2 {
    font-size: 2rem;
    font-weight: 700;
}

.features-wrapper {
display: flex;
flex-wrap: wrap;
justify-content: space-between;
margin-top: 55px;
}

.features-wrapper h3 {
    font-weight: 500;
    margin: 10px 0;
}

.features-wrapper .feature {
    width: 32%;
    margin-bottom: 70px;
}



@media screen and (max-width: 991px) {
    .features-wrapper .feature {
        width: 48%;
        margin-bottom: 70px;
    }
}

@media screen and (max-width: 767px) {
    .features-wrapper .feature {
        width: 100%;
        margin-bottom: 70px;
    }
}
</style>
