<template>
    <div class="FilterDoublerange">
        <h4 class="FilterDoublerange-title FilterDoublerange__title">Продолжительность</h4>
        <div class="FilterDoublerange-slider-wrap FilterDoublerange-slider__wrap">
            <p class="FilterDoublerange-count FilterDoublerange__count">От {{ value[0] }} до {{ value[1] }} мес.</p>
            <Slider v-model="value" :min="1" :max="6" :tooltips="false" />
        </div>
    </div>
</template>

<script>
    import Slider from '@vueform/slider'
    export default {
        components: { Slider },
        data: () => ({
            value: [1, 6],
        })
    }
</script>

<style lang="sass">
    @import "@vueform/slider/themes/default.css"
    @import "FilterDoublerange"
</style>