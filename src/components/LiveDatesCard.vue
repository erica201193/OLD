<template>
    <div>
        <div class="row px-5 py-5">
            <div class="col-4 event-map">
                <img :src="info.mapImg" alt="">
            </div>
            <div class="col event-description">
                <span>{{ info.artist }}</span>
                <p>{{ info.description }}</p>
                <button class="custom-btn btn-pink book-btn">book now</button>
            </div>
        </div>
    </div>
</template>

<script>


export default {
    props: {
        info: Object,
    }
}

</script>

<style lang="scss" scoped>

.bg-info {
    background-color: #323844;
}
.lessinfo-btn {
    height: 80%;
    aspect-ratio: 1/1;
    font-size: 50px;
    padding: 0rem .7rem .4rem .3rem;
    line-height: 1rem;
    font-weight: 400;
    border-radius: 0;
}

.event-map {
    img {
        max-width: 100%;
        height: 100%;
        object-fit: cover;
        box-shadow: 0rem 0.5rem 2rem rgba(black, .9);
    }
}

.event-description {
    text-transform: capitalize;
    padding-left: 2rem;
    span {
        color: white;
        letter-spacing: 2px;
        font-weight: 700;
    }
    p {
        font-size: 0.9rem;
        color: #6e798f;
        line-height: 2rem;
        margin-bottom: 0;
        padding: 1.5rem 0;
    }
}
.book-btn {
        font-weight: lighter;
        font-size: 0.9rem;
        padding: .6rem 1.6rem;
    }
</style>

