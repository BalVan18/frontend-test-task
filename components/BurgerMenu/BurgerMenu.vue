<template>
    <div class="BurgerMenu">
        <div class="BurgerMenu-btn BurgerMenu__btn" @click="burgerActive">
            <span class="BurgerMenu-btn-line BurgerMenu-btn__line line line--1"></span>
            <span class="BurgerMenu-btn-line BurgerMenu-btn__line line line--2"></span>
            <span class="BurgerMenu-btn-line BurgerMenu-btn__line line line--3"></span>
        </div>
        <nav class="BurgerMenu-nav BurgerMenu__nav">
            <ul class="BurgerMenu-nav-list BurgerMenu-nav__list">
                <li class="BurgerMenu-nav-list-item BurgerMenu-nav-list__item">
                    <a href="#" class="BurgerMenu-nav-list-item-link BurgerMenu-nav-list-item__link">
                    Курсы
                    </a>
                </li>
                <li class="BurgerMenu-nav-list-item BurgerMenu-nav-list__item">
                    <a href="#" class="BurgerMenu-nav-list-item-link BurgerMenu-nav-list-item__link">
                    Статьи
                    </a>
                </li>
                <li class="BurgerMenu-nav-list-item BurgerMenu-nav-list__item">
                    <a href="#" class="BurgerMenu-nav-list-item-link BurgerMenu-nav-list-item__link">
                    Вопросы
                    </a>
                </li>
            </ul>
            <img src="~/assets/img/search.png" alt="Иконка поиска" class="BurgerMenu-nav-search BurgerMenu-nav__search">
            <HeaderDropdown :options="['RU','EN']" />
        </nav>
    </div>
</template>

<script setup>
    const burgerActive = () => {
        const root = document.querySelector('.AppHeader');
        root.classList.toggle('active');
        document.body.classList.toggle('overflow');
    }
</script>

<style lang="sass" scoped>
  @import "BurgerMenu"
</style>
