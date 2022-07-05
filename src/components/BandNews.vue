<template>
    <div>
        <main>
            <!-- Section: MUSIC IS LIFE-->
            <div class="bg-grey">
                <div class="container">
                    <div class="custom-pink-hr"></div>
                    <div class="my-padding text-center">
                        <h2 class="py-3">Music Is Life</h2>
                        <div class="custom-hr my-3"></div>
                        <p class="py-3">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum finibus
                            cursus egestas. Cras quis vehicula <br> quam, a tempus velit. Ut feugiat augue in sodales
                            luctus</p>
                    </div>
                </div>
            </div>
            <!-- Section: BAND NEWS -->

            <div class="bg-darkgrey py-5">
                <div class="container">
                    <div class="py-5 text-center">
                        <h2 class="py-3">Latest Band News</h2>
                        <div class="custom-hr my-3"></div>
                        <p class="py-3">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum finibus
                            cursus egestas. Cras quis vehicula <br> quam, a tempus velit. Ut feugiat augue in sodales
                            luctus</p>
                    </div>

                    <div class="row justify-content-center">
                        <!-- <div class="col" v-for="article in blogPosts" :key="article.id">
                            <BlogCard :blog-card="article"></BlogCard>
                        </div> -->

                        <!-- Sezione News SINISTRA -->
                        <div class="col-8 row">

                            <div class="col-12 pb-4">
                                <div class="news-card horizontal-card">
                                    <img :src="blogPosts[0].image" alt="">
                                    <div class="card-text">
                                        <h5>{{ blogPosts[0].title }}</h5>
                                        <p>{{ blogPosts[0].subtitle }}</p>
                                    </div>
                                    <h5 class="hover-text">{{ blogPosts[0].title }}</h5>
                                    <div class="hover-red-filter"></div>
                                </div>
                            </div>

                            <div class="col-6">
                                <div class="news-card vertical-card">
                                    <img :src="blogPosts[2].image" alt="">
                                    <div class="card-text ">
                                        <h5>{{ blogPosts[2].title }}</h5>
                                        <p>{{ blogPosts[2].subtitle }}</p>
                                    </div>
                                    <h5 class="hover-text">{{ blogPosts[2].title }}</h5>
                                    <div class="hover-red-filter"></div>
                                </div>
                            </div>

                            <div class="col-6">
                                <div class="news-card vertical-card">
                                    <img :src="blogPosts[3].image" alt="">
                                    <div class="card-text ">
                                        <h5>{{ blogPosts[3].title }}</h5>
                                        <p>{{ blogPosts[3].subtitle }}</p>
                                    </div>
                                    <h5 class="hover-text">{{ blogPosts[3].title }}</h5>
                                    <div class="hover-red-filter"></div>
                                </div>
                            </div>

                            <div class="col-12 pt-4">
                                <div class="news-card horizontal-card">
                                    <img :src="blogPosts[5].image" alt="">
                                    <div class="card-text ">
                                        <h5>{{ blogPosts[5].title }}</h5>
                                        <p>{{ blogPosts[5].subtitle }}</p>
                                    </div>
                                    <h5 class="hover-text">{{ blogPosts[5].title }}</h5>
                                    <div class="hover-red-filter"></div>
                                </div>
                            </div>
                        </div>

                        <!-- Sezione News DESTRA -->
                        <div class="col-4 row flex-column">

                            <div class="col d-flex grow-1 pb-2">
                                <div class="news-card vertical-card">
                                    <img :src="blogPosts[1].image" alt="">
                                    <div class="card-text ">
                                        <h5>{{ blogPosts[1].title }}</h5>
                                        <p>{{ blogPosts[1].subtitle }}</p>
                                    </div>
                                    <h5 class="hover-text">{{ blogPosts[1].title }}</h5>
                                    <div class="hover-red-filter"></div>
                                </div>
                            </div>

                            <div class="col d-flex grow-1 pt-3">
                                <div class="news-card vertical-card">
                                    <img :src="blogPosts[4].image" alt="">
                                    <div class="card-text ">
                                        <h5>{{ blogPosts[4].title }}</h5>
                                        <p>{{ blogPosts[4].subtitle }}</p>
                                    </div>
                                    <h5 class="hover-text">{{ blogPosts[4].title }}</h5>
                                    <div class="hover-red-filter"></div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="banner-btn row text-center">
                <a href="#">view all latest news</a>
            </div>




        </main>
    </div>
</template>

<script>

export default {
    data() {
        return {
            blogPosts: [
                {
                    id: "1",
                    image: "img/blog_music_techo.jpg",
                    title: "Technology and music",
                    subtitle: "Sed sit amet sem turpis. Curabitur cursus lacinia est at interdum risus id condimentum.",
                },
                {
                    id: "2",
                    image: "img/blog-post1.jpg",
                    title: "Taking it back to the old school",
                    subtitle: "Sed sit amet sem turpis. Curabitur cursus lacinia est at interdum risus id condimentum.",
                },
                {
                    id: "3",
                    image: "img/blog-post3.jpg",
                    title: "While my guitar gently weeps",
                    subtitle: "Sed sit amet sem turpis. Curabitur cursus lacinia est at interdum risus id condimentum.",
                },
                {
                    id: "4",
                    image: "img/blog-post4.jpg",
                    title: "It just sounds better",
                    subtitle: "Sed sit amet sem turpis. Curabitur cursus lacinia est at interdum risus id condimentum.",
                },
                {
                    id: "5",
                    image: "img/blog-post2.jpg",
                    title: "Sharing the stage with a legend",
                    subtitle: "Sed sit amet sem turpis. Curabitur cursus lacinia est at interdum risus id condimentum.",
                },
                {
                    id: "6",
                    image: "img/blog_flavor_rock.jpg",
                    title: "The flavor of rock",
                    subtitle: "Sed sit amet sem turpis. Curabitur cursus lacinia est at interdum risus id condimentum.",
                }
            ],
            hover: false,
        };
    },
    methods: {
    }
}

</script>

<style lang="scss">

.container {
    h2 {
        font-size: 60px;
        font-weight: 700;
    }
    h5 {
        font-size: 1.1rem;
    }
    p {
        font-family: 'Merriweather', serif;
        font-size: .95rem;
    }
}

.bg-grey {
    background-color: #323844;
}

.bg-darkgrey {
    background-color: #252A33;
}

.custom-pink-hr {
    width: 100%;
    max-width: 500px;
    height: 16px;
    background-color: #ea4a56;
    margin: 0 auto;
}

.custom-hr {
    width: 100%;
    max-width: 300px;
    height: 2px;
    background-color: #7780a464;
    margin: 0 auto;
}

.banner-btn {
    a {
        text-decoration: none;
        text-transform: uppercase;
        font-weight: 700;
        font-size: 18px;
        color: #fff;
        background-color: #eb4b54;
        padding: 60px;
        transition: 0.3s ease-in-out;

        &:hover {
            color: #0b2037;
            background-color: white;
        }
        
    }
    
}

// CARDS

.horizontal-card {
    height: 300px;
}
.news-card {
    position: relative;
    border: 1px solid #323844;

    &:hover {
        cursor: pointer;
        .card-text {
            opacity: 0%;
        }
        .hover-text {
            opacity: 100%;
        }
        .hover-red-filter {
            opacity: 0.7;
        }
    }
    
    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: center;
            
        }
    .card-text {
        text-align: left;
        position: absolute;
        bottom: 0;
        background-color: #323844;
        width: 100%;
        padding: 1.75rem;
        h5 {
            color: #ea4a56;
            font-weight: 700;
            margin-bottom: 0;
            padding-bottom: .5rem;
        }
        p {
            color: #aeaeaf;
            margin-bottom: 0;
        }
    }

}
.hover-red-filter {
    width: 100%;
    height: 100%;
    background-color: #ea4a56;
    position: absolute;
    top: 0;
    opacity: 0;

}

.hover-text {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    width: 100%;
    color: white;
    font-weight: 700;
    opacity: 0;
    z-index: 2;
}
</style>