<template>
    <div>
        <div class="bg-videoplayer py-5">
            <div class="container">
                <div class="row pt-4 justify-content-center align-items-center text-center">
                    <div class="col">
                        <p class="video-quote mb-5">
                            "I just listened to it and said to myself, "Man, I really love this <br>
                            album." Still, today, it just sounds so fresh. It sounds full of <br>
                            ideas. These guys knew what they were doing. They're good. <br>
                            And they're inventive. I haven't heard anything this year <br>
                            that's as inventive. I don 't really expect to."
                        </p>
                        <div class="videoWrapper mb-5">
                        <iframe width="560" height="315" src="https://www.youtube.com/embed/WvdYFFkOgAA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                        </div>
                        
                        <div class="player-btn ">
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
    height: 100vh;
    p {
        font-size: 1.5rem;
    }
}
.video-quote {
    font-weight: 700;
    font-style: italic;
    line-height: 44px;
    
}

.player-btn {
    cursor: pointer;
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