<template>
    <div class="portfolio with-caption">
        <div class="thumb video-with-thumb">
            <img class="img-thumbnail rounded img-fluid" :src="portfolio.image" :alt="portfolio.heading">
        </div>
        <div class="caption-bottom text-start">
            <div class="info">
                <h5 class="h5 theme-color">
                        {{ portfolio.heading }}
                </h5>
                <p class="bk_pra theme-color-2">{{ portfolio.category }}</p>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props: ["portfolio"]
    };
</script>
