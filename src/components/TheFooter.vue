<template>
    <div>
        <div class="bg-grey">
            <div class="container">
                <div class="row my-padding">
                    <div class="col-3 text-start">
                        <img src="../../public/img/logo_footer.png" alt="">
                    </div>
                    <div class="col d-flex align-items-center justify-content-end">
                        <ul class="link-list">
                            <li v-for="link in footerLinks" :key="link.link"> <a href="link.href">{{ link.link }}</a> </li>
                        </ul>
                    </div>               
                </div>
            </div>
        </div>

        <div class="bg-footer">
            <div class="container">
                <div class="row py-4">
                    <div class="col text-start copyright-info">
                        <p>© Copyright 2012 - 2022 | Avada Theme by ThemeFusion | All Rights Reserved | Powered by WordPress</p>
                    </div>
                    <div class="col social-links">
                        <a
                            v-for="socialLink in socialLinks" :key="socialLink.name" href="socialLink.href">
                            <i :class="socialLink.icon"></i>
                        </a>
                    </div>               
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            footerLinks: [
                {
                    link: "Home",
                    href: "#",
                    logo: "fa-brands fa-facebook-f fa-x"
                },
                {
                    link: "Meet The Band",
                    href: "#",
                },
                {
                    link: "Live Dates",
                    href: "#",
                },
                {
                    link: "Latest News",
                    href: "#",
                },
                {
                    link: "Albums",
                    href: "#",
                },
                {
                    link: "Fans",
                    href: "#",
                },
            ],
            socialLinks: [
                {
                    name: "Facebook",
                    href: "#",
                    icon: "fa-brands fa-facebook-f"
                },
                {
                    name: "Twitter",
                    href: "#",
                    icon: "fa-brands fa-twitter"
                },
                {
                    name: "Instagram",
                    href: "#",
                    icon: "fa-brands fa-instagram"
                },
                {
                    name: "YouTube",
                    href: "#",
                    icon: "fa-brands fa-youtube"
                },
            ]
        };
    },
}

</script>

<style lang="scss">

.bg-footer {
    background-color: #292d39;
}
.my-padding {
    padding: 60px 0px;
}
.link-list {
    list-style-type: none;
    display: flex;
    margin-bottom: 0;
    font-weight: 700;
    font-family: 'Merriweather', serif;
    font-size: 0.8rem;

    a {
        color: #6b6b6c;
        padding: 2rem 1rem;
        transition: 0.3s ease-in-out;

        &:hover {
                color:  #fff;
            }
    }
}

.copyright-info {
    font-size: 0.7rem;
    display: flex;
    align-items: center;
    p {
        margin-bottom: 0;
    }
}
.social-links {
    display: flex;
    gap: 1rem;
    justify-content: end;
    align-items: center;

    a {
        font-size: 1.2rem;
        color: #6b6b6c;
        background-color: #323844;;
        width: 40px;
        aspect-ratio: 1/1;
        transition: 0.3s ease-in-out;
        margin-bottom: 0;
        display: flex;
        justify-content: center;
        align-items: center;


        &:hover {
            color:  #fff;
        }
    }
}
</style>