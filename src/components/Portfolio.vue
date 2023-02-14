<template>
    <section>
        <div class="project" v-for="project, key in projects" :key="key">
            <div class="img-wrapper">
                <div class="overlay"></div>
                <img :src="project.image" :alt="project.alt">
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
                image: "./src/assets/images/home-one.jpg",
                caption: "Home One",
                alt: "Home one"
            },
            {
                image: "./src/assets/images/home-two.jpg",
                caption: "Home Two",
                alt: "Home two"
            },
            {
                image: "./src/assets/images/home-three.jpg",
                caption: "Home Three",
                alt: "Home three"
            },
            {
                image: "./src/assets/images/blog.jpg",
                caption: "Blog",
                alt: "Blog"
            },
            {
                image: "./src/assets/images/blog-details.jpg",
                caption: "Blog Details",
                alt: "Blog details"
            },
            {
                image: "./src/assets/images/categories.jpg",
                caption: "Categories",
                alt: "Categories"
            },
            {
                image: "./src/assets/images/about.jpg",
                caption: "About",
                alt: "About"
            },
            {
                image: "./src/assets/images/faq.jpg",
                caption: "FAQ",
                alt: "FAQ"
            },
            {
                image: "./src/assets/images/contact.jpg",
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