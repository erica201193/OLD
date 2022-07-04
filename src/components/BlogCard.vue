<template>
    <div>
        <div class="card">
            <img :src="blogCard.image" alt="">
            <p><strong>{{ blogCard.title }}</strong></p>
            <p>{{ blogCard.subtitle }}</p>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        blogCard: Object,
    }
}
</script>