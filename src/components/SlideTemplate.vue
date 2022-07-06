<template>
    <div class="">
        <div class="slide-template text-center mb-5 position-relative">
            <img :src="img" alt="" class="my-5">
            <transition class="py-5 position-relative">
                <h5 v-show="select" class="mt-5">{{ eventName }}</h5>
            </transition>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        img: String,
        eventName: String,
        select: Boolean,
    }
}
</script>

<style lang="scss" scoped>

.v-enter-active,
.v-leave-active {
  transition: opacity 0.4s ease-in-out;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}

h5 {
    color: rgba(255, 255, 255, 0.6);
    font-size: .9rem;
    padding: 1.5rem 0rem;
    position: absolute;
    top: 0;
    }
.slide-template {
    img {
        max-width: 100%;
        aspect-ratio: 1/1;
        object-fit: cover;
        object-position: bottom;
        overflow: hidden;
        box-shadow: 0rem 0.5rem 2rem rgba(black, .5);
        transition: all 0.5s ease-in-out;
        position: relative;
        top: 0;

        &:hover {
            transform: scale(1.2);
            object-position: bottom;
            position: relative;
            top:50px;
            h5 {
                opacity: 100%;
            }
        }

    }
}
</style>