<template>
    <div class="FilterDropdown" ref="dropDown" :class="isDropDownVisible ? 'visible' : ''">
        <div class="FilterDropdown-btn FilterDropdown__btn" @click="isDropDownVisible=true">
            <span class="FilterDropdown-btn-text FilterDropdown-btn__text">{{ selectedOption || "Язык" }}</span>
            <svg class="FilterDropdown-btn-svg FilterDropdown-btn__svg" width="15" height="7.5" viewBox="0 0 17 10" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M1 1L8.5 8.5" stroke="black" stroke-width="2" stroke-linecap="round"/>
                <path d="M16 1L8.5 8.5" stroke="black" stroke-width="2" stroke-linecap="round"/>
            </svg>
        </div>
        <transition name="slide-fade">
            <div class="FilterDropdown-wrap FilterDropdown__wrap" v-if="isDropDownVisible">
                <option class="FilterDropdown-option FilterDropdown__option" v-for="(option) in props.options" @click="toggleOptionSelect(option)">{{ option }}</option>
            </div>
        </transition>
    </div>
</template>

<script setup>
    import { ref, onMounted, onBeforeUnmount } from 'vue';

    const props = defineProps({
        options: {
            type: Array
        }
    })

    let dropDown = ref (null),
        selectedOption = ref (null),
        isDropDownVisible = ref (false)



    let toggleOptionSelect = (option)=> {
        selectedOption.value=option
        isDropDownVisible.value=false
    }


    let closeDropDown = (element)=> {
        if (!dropDown.value.contains(element.target)) {
            isDropDownVisible.value = false
        }
    }

    onMounted(()=> {
        window.addEventListener('click', closeDropDown)
    })

    onBeforeUnmount(()=> {
        window.removeEventListener('click', closeDropDown)
    })
</script>

<style lang="sass" scoped>
  @import "FilterDropdown.sass"
</style>