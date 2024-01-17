<template>
    <div class="MainFilterMedia">
        <div class="MainFilterMedia-wrap MainFilterMedia__wrap">
            <FilterDropdown :options="['Русский','Английский']"/>
            <div class="MainFilterMedia-btn MainFilterMedia__btn" @click="filterActive"></div>
        </div>
        <div class="MainFilterMedia-settings MainFilterMedia__settings hidden">
                <FilterDoublerange />
                <FilterRadio />
                <FilterCheckbox />
            </div>
    </div>
</template>

<script setup>
    const filterActive = () => {
        const wrap = document.querySelector('.MainFilterMedia')
        const filter = document.querySelector('.MainFilterMedia-settings')
        filter.classList.toggle('hidden')
        wrap.classList.toggle('active')
    }
</script>

<style lang="sass">
    @import "MainFilterMedia"
</style>