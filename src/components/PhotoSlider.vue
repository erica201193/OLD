<template>
    <div class="bg-darkgrey">
        <div class="container position-relative py-5">

            <div class="row align-items-center row-cols-3 photo-slider" id="slider">
                <div class="col" v-for="(slide, i) in eventPhotos" :key="i + 1"
                    @mouseenter="selectImg(slide)"
                    @mouseleave="deselectImg(slide)">
                    <SlideTemplate :img="slide.photo" :eventName="slide.eventName" :select="slide.select">
                    </SlideTemplate>
                </div>
            </div>
            <div class="row pt-3">
                <div class="col left-scroll slider-btn" @click="scroll('prev')">
                    <i class="fa-solid fa-circle-chevron-left fa-lg"></i>
                </div>
                <div class="col right-scroll slider-btn" @click="scroll('next')">
                    <i class="fa-solid fa-circle-chevron-right fa-lg"></i>
                </div>
            </div>


        </div>


    </div>
</template>

<script>
import SlideTemplate from './SlideTemplate.vue';

export default {
    name: 'PhotoSlider',
    components: { SlideTemplate },
    data() {
        return {
            eventPhotos: [
                {
                    date: "11/05/2022",
                    eventName: "SoundWeek Barcelona Festival",
                    photo: "/img/slider_1.jpg",
                    select: false,
                },
                {
                    date: "11/05/2022",
                    eventName: "Coachella 2022",
                    photo: "/img/slider_3.jpg",
                    select: false,
                },
                {
                    date: "11/05/2022",
                    eventName: "Eurovision 2022",
                    photo: "/img/slider_2.jpg",
                    select: false,
                },
                {
                    date: "23/02/2022",
                    eventName: "SoulFestival Milan",
                    photo: "/img/slider_4.jpeg",
                    select: false,
                },
                {
                    date: "23/02/2022",
                    eventName: "Amsterdam MusicFest",
                    photo: "/img/slider_5.jpeg",
                    select: false,
                },
                {
                    date: "23/02/2022",
                    eventName: "Athena Stadium 2018",
                    photo: "/img/slider_6.jpeg",
                    select: false,
                },
                

            ],
        };
    },
    methods: {
        scroll(direction) {
            const slider = document.getElementById("slider");

            if (direction == "next") {
                slider.scrollBy({
                left: 500,
                behavior: 'smooth'
            })
            } else if (direction == "prev") {
                slider.scrollBy({
                    left: -500,
                    behavior: 'smooth'
                })
            }
        },

        selectImg(slide) {
            slide.select = true;
            console.log(slide.select);
        },

        deselectImg(slide) {
            slide.select = false;
            console.log(slide.select);
        }
        
    }
}

</script>

<style lang="scss" scoped>

.photo-slider {
    overflow: auto;
    flex-wrap: nowrap;
}

.slider-btn {
    transition: 0.3s ease-in-out;
    color: rgba(255, 255, 255, 0.4);
    z-index: 999;
    
    &:hover, &:active {
        cursor: pointer;
        color: white;
    }
}
.left-scroll {
text-align: end;
}
</style>

