<template>
    <div class="FilterRadio">
        <h4 class="FilterRadio-title FilterRadio__title">Сложность</h4>
            <label class="FilterRadio-label FilterRadio__label" @click="e => e.target.classList.toggle('checked')">
                <span class="FilterRadio-text FilterRadio__text">Для всех</span>
            </label>
            <label class="FilterRadio-label FilterRadio__label" @click="e => e.target.classList.toggle('checked')">
                <span class="FilterRadio-text FilterRadio__text">Для начинающих</span>
            </label>
            <label class="FilterRadio-label FilterRadio__label" @click="e => e.target.classList.toggle('checked')">
                <span class="FilterRadio-text FilterRadio__text">Продвинутый уровень</span>
            </label>
    </div>
</template>

<script>
</script>

<style lang="sass">
    @import "FilterRadio.sass"
</style>