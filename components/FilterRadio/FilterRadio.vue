<template>
    <div class="FilterRadio">
        <h4 class="FilterRadio-title FilterRadio__title">Сложность</h4>
            <label class="FilterRadio-label FilterRadio__label">
                <input type="radio" name="FilterRadio" class="FilterRadio-input FilterRadio__input">
                <span class="FilterRadio-text FilterRadio__text" @click="checked">Для всех</span>
            </label>
            <label class="FilterRadio-label FilterRadio__label">
                <input type="radio" name="FilterRadio" class="FilterRadio-input FilterRadio__input">
                <span class="FilterRadio-text FilterRadio__text" @click="checked">Для начинающих</span>
            </label>
            <label class="FilterRadio-label FilterRadio__label">
                <input type="radio" name="FilterRadio" class="FilterRadio-input FilterRadio__input">
                <span class="FilterRadio-text FilterRadio__text" @click="checked">Продвинутый уровень</span>
            </label>
    </div>
</template>

<script setup>
    const checked = (e) => {
        const labels = document.querySelectorAll('.FilterRadio-label')
        labels.forEach(label => {
            label.classList.remove('checked')
        });
        const parent = e.target.parentNode
        parent.classList.toggle('checked')
    }
</script>

<style lang="sass" scoped>
    @import "FilterRadio.sass"
</style>