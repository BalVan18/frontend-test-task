<template>
    <div class="MainFilter">
        <FilterDropdown :options="['Русский','Английский']" />
        <FilterDoublerange />
        <FilterRadio />
        <FilterCheckbox />
    </div>
</template>

<style lang="sass" scoped>
    @import "MainFilter"
</style>