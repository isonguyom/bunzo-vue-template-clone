<template>
    <section>
        <div class="project" v-for="project, key in projects" :key="key">
            <div class="img-wrapper">
                <div class="overlay"></div>
                <img :src="`images/${project.image}`" :alt="project.alt">
            </div>
            <a href="" class="caption">{{ project.caption }}</a>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            projects: [
                {
                    image: "home-one.jpg",
                    caption: "Home One",
                    alt: "Home one"
                },
                {
                    image: "home-two.jpg",
                    caption: "Home Two",
                    alt: "Home two"
                },
                {
                    image: "home-three.jpg",
                    caption: "Home Three",
                    alt: "Home three"
                },
                {
                    image: "blog.jpg",
                    caption: "Blog",
                    alt: "Blog"
                },
                {
                    image: "blog-details.jpg",
                    caption: "Blog Details",
                    alt: "Blog details"
                },
                {
                    image: "categories.jpg",
                    caption: "Categories",
                    alt: "Categories"
                },
                {
                    image: "about.jpg",
                    caption: "About",
                    alt: "About"
                },
                {
                    image: "faq.jpg",
                    caption: "FAQ",
                    alt: "FAQ"
                },
                {
                    image: "contact.jpg",
                    caption: "Contact",
                    alt: "Contact"
                }
            ]
        }
    }
}

</script>

<style scoped>
section {
    padding: 110px 7%;
    display: flex;
    flex-flow: wrap;
    justify-content: space-between;
}


.project {
    width: 32%;
    height: fit-content;
    box-shadow: 0 0 15px rgb(0 0 0 / 15%);
    text-align: center;
    padding-bottom: 20px;
    margin-bottom: 60px;
}

.project .img-wrapper {
    width: fit-content;
    height: fit-content;
    position: relative;
    transition: all 0.3s ease 0s;
}

.project .img-wrapper .overlay {
    width: 100%;
    height: 100%;
    background-color: #5038eea4;
    position: absolute;
    z-index: 1;
    display: none;
}

.project:hover .overlay {
    display: block;
    transition: all .4s ease;
}

.project:hover .img-wrapper {
    transform: translateY(-10px);
}

.project a {
    display: block;
    text-decoration: none;
    text-transform: uppercase;
    color: #373737;
    font-weight: 600;
    margin: 20px 0 5px;
}

.project a:hover {
    color: #5138EE;
}


@media screen and (max-width: 991px) {
    .project {
        width: 48%;
    }
}

@media screen and (max-width: 767px) {
    section {
        justify-content: center;
    }

    .project {
        width: fit-content;
    }
}
</style>