<template>
        <div class="content">
            <h4 class="heading heading-h4">{{ testimonial.title }}</h4>
            <ul class="rating d-flex">
                <li><i class="fa fa-star"></i></li>
                <li><i class="fa fa-star"></i></li>
                <li><i class="fa fa-star"></i></li>
                <li><i class="fa fa-star"></i></li>
                <li><i class="fa fa-star"></i></li>
            </ul>
            <p class="bk_pra">{{ testimonial.text }}</p>
            <div class="testimonial-info">
                <div class="post-thumbnail">
                    <img :src="testimonial.thumb" :alt="testimonial.alt">
                </div>
                <div class="clint-info">
                    <h6>{{ testimonial.name }}</h6>
                    <span>{{ testimonial.position }}</span>
                </div>
                <div class="testimonial-quote">
                    <span class="fa fa-quote-right"></span>
                </div>
            </div>
        </div>
</template>


<script>
    export default {
        props: ["testimonial"]
    };
</script>
