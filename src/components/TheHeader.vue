<template>

    <div class="">
        <div class="bg-jumbotron">
            <div class="container-fluid px-5 text-center">
                <nav class="d-flex justify-content-between align-items-center pt-3">
                    <img src="/img/avada-music-logo-retina.png" alt="" class="navbar-logo">
                    <button @click="openMenu" class="navbar-toggle btn"><i class="fa-solid fa-bars fa-2x"></i></button>
                </nav>
                <div class="jumbo">
                    <h1 class="fw-bold m-0">Untold Stories</h1>
                    <span class="">There is untold story behind every favourite song.</span>
                    <div class="">
                        <button class="custom-btn btn-pink mx-2">latest album</button>
                        <button class="custom-btn btn-transparent mx-2">live dates</button>
                    </div>
                </div>
            </div>
        </div>
        <transition>
            <div class="bg-menu" v-if="isVisible === true">
                <div class="container-fluid px-5 text-center">
                    <nav class="d-flex justify-content-between align-items-center pt-3">
                        <img src="/img/avada-music-logo-retina.png" alt="" class="navbar-logo">
                        <button @click="closeMenu" class="navbar-toggle btn"><i
                                class="fa-solid fa-bars fa-2x"></i></button>
                    </nav>
                    <div class="jumbo">
                        <ul class="list-unstyled">
                            <li v-for="link in headerLinks" :key="link.link">
                                <a href="link.href" class="menu-links">{{ link.link }}</a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </transition>

    </div>
</template>


<script>
export default {
    data() {
        return {
            headerLinks: [
                {
                    link: "Home",
                    href: "#home",
                    logo: "fa-brands fa-facebook-f fa-x"
                },
                {
                    link: "Meet The Band",
                    href: "#meet",
                },
                {
                    link: "Live Dates",
                    href: "#live_dates",
                },
                {
                    link: "Latest News",
                    href: "#news",
                },
                {
                    link: "Albums",
                    href: "#albums",
                },
                {
                    link: "Fans",
                    href: "#fans",
                },
            ],
            isVisible: false,
        };
    },
    methods: {
        openMenu() {
            this.isVisible = true;
        },
        closeMenu() {
            this.isVisible = false;
        }
    }
}

</script>


<style lang="scss">


.v-enter-active,
.v-leave-active {
  transition: opacity 0.5s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}


.bg-jumbotron {
    background-image: url("../../public/img/home_slider.jpg");
    background-size: cover;
    background-position: center;
    height: 100vh;
    width: 100vw;
}
    .jumbo {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 100%;
        h1 {
            font-size: 150px;
        }
        span {
            font-family: 'Merriweather', sans-serif;
            font-size:24px;
            display: block;
            margin-top: 0.5rem;
            margin-bottom: 3rem;
        }
    }

.navbar-toggle {
    color: white!important;

    &:hover {
        border-width: 2px!important;;
    }
}

.bg-menu {
    height: 100vh;
    width: 100vw;
    background-color: #ea4a56;
    position: absolute;
    top: 0;
}

.menu-links {
    color: rgba(255, 255, 255, 0.6);
    font-family: 'Merriweather', sans-serif;
    font-weight: 700;
    font-size: 28px;
    display: block;
    margin-top: 0.5rem;
    margin-bottom: 3rem;
    &:hover {
        color: white;
    }
}

.activelink {
    color: white;
}

.navbar-logo {
    height: 75px;
}

.custom-btn {
    text-transform: uppercase;
    display: inline-block;
    font-weight: 700;
    text-align: center;
    vertical-align: middle;
    user-select: none;
    border: 1px solid transparent;
    box-shadow: 1px black;
    padding: .8rem 2.5rem;
    font-size: 18px;
    letter-spacing: 2px;
    line-height: 1.5rem;
    border-radius: 0.1rem;
    transition: color .15s ease-in-out,background-color .15s ease-in-out,border-color .15s ease-in-out,box-shadow .15s ease-in-out;
    
    &:hover {
        color: #0b2037;
        background-color: white;
        border-color: white;
    }
}

.btn-pink {
    color: #fff;
    background-color: #eb4b54;
    border-color: #eb4b54;
}

.btn-transparent {
    color: #fff;
    background-color: transparent;
    border-color: #fff;
}



</style>