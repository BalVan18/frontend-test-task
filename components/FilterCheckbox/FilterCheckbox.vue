<template>
    <div class="FilterCheckbox">
        <h4 class="FilterCheckbox-title FilterCheckbox__title">Навыки</h4>
        <label class="FilterCheckbox-label FilterCheckbox__label" @click="e => e.target.classList.toggle('checked')">
            <span class="FilterCheckbox-text FilterCheckbox__text">Грамматика</span>
        </label>
        <label class="FilterCheckbox-label FilterCheckbox__label" @click="e => e.target.classList.toggle('checked')">
            <span class="FilterCheckbox-text FilterCheckbox__text">Лексика</span>
        </label>
        <label class="FilterCheckbox-label FilterCheckbox__label" @click="e => e.target.classList.toggle('checked')">
            <span class="FilterCheckbox-text FilterCheckbox__text">Синтаксис</span>
        </label>
        <label class="FilterCheckbox-label FilterCheckbox__label" @click="e => e.target.classList.toggle('checked')">
            <span class="FilterCheckbox-text FilterCheckbox__text">Фонетика</span>
        </label>
        <label class="FilterCheckbox-label FilterCheckbox__label" @click="e => e.target.classList.toggle('checked')">
            <span class="FilterCheckbox-text FilterCheckbox__text">Пунктуация</span>
        </label>
    </div>
</template>

<script>
</script>

<style lang="sass" scoped>
    @import "FilterCheckbox"
</style>