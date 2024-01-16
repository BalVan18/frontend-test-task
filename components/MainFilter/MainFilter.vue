<template>
    <div class="MainFilter">
        <FilterDropdown :options="options" />
        <FilterDoublerange />
        <FilterRadio />
        <FilterCheckbox />
    </div>
</template>

<script setup>
    import { ref } from 'vue';
    const options = ref(["Русский", "Английский"])
</script>

<style lang="sass" scoped>
    @import "MainFilter.sass"
</style>