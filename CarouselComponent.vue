<script setup>
import { Carousel } from 'flowbite-vue'

const props = defineProps({
    pictures: {
        type: Array,
        default() {
            return [
                {
                    'src': 'https://jkt48.com/images/banner.fanclub2021-id.jpg',
                    'alt': 'Picture 1',
                },
                {
                    'src': 'https://assets.pikiran-rakyat.com/crop/0x0:0x0/x/photo/2022/02/11/1781638866.png',
                    'alt': 'Picture 2',
                },
            ]
        },
    },
})

</script>
<template>
  <Carousel :pictures="pictures" :indicators="false"></Carousel>
</template>
