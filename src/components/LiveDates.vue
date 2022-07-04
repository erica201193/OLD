<template>
    <div class="bg-darkgrey py-5">
        <div class="container">
            <div class="py-5 text-center">
                <h2 class="py-3">Live Dates</h2>
                <div class="custom-hr my-3"></div>
                <p class="py-3">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum finibus cursus
                    egestas. Cras quis vehicula <br> quam, a tempus velit. Ut feugiat augue in sodales luctus</p>
            </div>

            <div class="event-info ps-3 event-info-list row" v-for="(event, i) in liveDates" :key="i"
                @click="showInfo(event)">
                <div class="col">
                    <div v-if="event.open === false" class="d-inline">
                        <button class="custom-btn moreinfo-btn">+</button>
                    </div>
                    <div v-else class="d-inline">
                        <button class="custom-btn moreinfo-btn">-</button>
                    </div>

                    <h5 class="ms-3 d-inline">
                        {{ event.date }}
                        {{ event.event }}
                        {{ event.location }}
                    </h5>
                </div>

                <div v-if="event.open === true">
                    <LiveDatesCard :info="event"></LiveDatesCard>
                </div>
            </div>
        </div>

        <div class="banner-btn row text-center">
            <a href="#">view all live dates</a>
        </div>
    </div>
</template>

<script>
import LiveDatesCard from './LiveDatesCard.vue';
export default {
    components: { LiveDatesCard },
    data() {
        return {
            liveDates: [
                {
                    date: "17/08/2020",
                    event: "GEM FESTIVAL 2020",
                    location: "ANAKALIA, GEORGIA",
                    mapImg: "img/google_maps.jpeg",
                    artist: "Untold Stories",
                    description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
                    open: false,
                },
                {
                    date: "24/09/2020",
                    event: "GROOVEFEST",
                    location: "DOMINICAL REPUBLIC",
                    mapImg: "img/google_maps.jpeg",
                    artist: "Untold Stories",
                    description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
                    open: false,
                },
                {
                    date: "31/10/2020",
                    event: "OASIS FESTIVAL 2020",
                    location: "MARRAKECH, MOROCCO",
                    mapImg: "img/google_maps.jpeg",
                    artist: "Untold Stories",
                    description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
                    open: false,
                },
                {
                    date: "07/11/2020",
                    event: "MOGA FESTIVAL",
                    location: "ESSAOURIA, MOROCCO",
                    mapImg: "img/google_maps.jpeg",
                    artist: "Untold Stories",
                    description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
                    open: false,
                },
                {
                    date: "10/12/2020",
                    event: "ENVISION FESTIVAL",
                    location: "UVITA, COSTA RICA",
                    mapImg: "img/google_maps.jpeg",
                    artist: "Untold Stories",
                    description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
                    open: false,
                },

            ],
        };
    },
    methods: {
        showInfo(event) {
            if (event.open === false) {
            event.open = true;
            } else {
                event.open = false;
            }
            
        }
    }
}

</script>

<style lang="scss">

.event-info {
background-color: #323844;
color: #ea4a56;
text-transform: uppercase;
padding: 0.5rem 0;
margin-bottom: 1rem;
    h5 {
        font-weight: 700;
        align-self: center;
        margin-bottom: 0;
    }
}

.event-info-list {
    cursor: pointer;
    transition: all 0.5s ease 0s;
    &:hover {
        h5 {
            color: white;
        }
        .moreinfo-btn {
            color: white;
            background-color: #ea4a56;
            border-color: #ea4a56;
        }
    }
}
.moreinfo-btn {
    padding: 0 0.4rem;
    font-size: 20px;
    color: #fff;
    background-color: transparent;
    border-radius: 0;
}
</style>

