<template>
    <div class="slide-template text-center">
        <img :src="img" alt="" class="mb-5">
        <h5 class="mt-5">{{ eventName }}</h5>
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
.slide-template {
    img {
        max-width: 100%;
        aspect-ratio: 1/1;
        object-fit: cover;
        object-position: bottom;
        overflow: hidden;
        box-shadow: 0rem 0.5rem 2rem rgba(black, .5);
        transition: 0.5s ease-in-out;

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
    h5 {
        color: rgba(255, 255, 255, 0.243);
        font-size: .9rem;
        padding: 1.5rem 0rem;
        transition: 0.5s ease-in-out;
    }
}
</style>