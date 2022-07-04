<template>
    <div>
        <div class="bg-videoplayer py-5">
            <div class="container">
                <div class="row pt-4 justify-content-center align-items-center text-center">
                    <div class="col">
                        <p class="video-quote">
                            "I just listened to it and said to myself, "Man, I really love this <br>
                            album." Still, today, it just sounds so fresh. It sounds full of <br>
                            ideas. These guys knew what they were doing. They're good. <br>
                            And they're inventive. I haven't heard anything this year <br>
                            that's as inventive. I don 't really expect to."
                        </p>
                        <div class="player-btn">
                            <i class="fa-solid fa-play"></i>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script></script>

<style lang="scss">
.bg-videoplayer {
    background-image: url("../../public/img/home-testimonial-parallax.jpg");
    background-size: cover;
    background-position: center;
}
.video-quote {
    font-weight: 700;
    font-style: italic;
    font-size: 22px;
    line-height: 44px;
}

.player-btn {
    width: 100px;
    aspect-ratio: 1/1;
    border-radius: 50%;
    background-color: #eb4b54;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto;
    i {
        font-size: 25px;
    }
}

</style>