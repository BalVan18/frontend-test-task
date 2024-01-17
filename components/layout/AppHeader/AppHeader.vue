<template>
    <header class="AppHeader container">
      <AppLogo />
      <nav class="AppHeader-nav AppHeader__nav">
        <ul class="AppHeader-nav-list AppHeader-nav__list">
          <li class="AppHeader-nav-list-item AppHeader-nav-list__item">
            <a href="#" class="AppHeader-nav-list-item-link AppHeader-nav-list-item__link">
              Курсы
            </a>
          </li>
          <li class="AppHeader-nav-list-item AppHeader-nav-list__item">
            <a href="#" class="AppHeader-nav-list-item-link AppHeader-nav-list-item__link">
              Статьи
            </a>
          </li>
          <li class="AppHeader-nav-list-item AppHeader-nav-list__item">
            <a href="#" class="AppHeader-nav-list-item-link AppHeader-nav-list-item__link">
              Вопросы
            </a>
          </li>
        </ul>
        <img src="~/assets/img/search.png" alt="Иконка поиска" class="AppHeader-nav-search AppHeader-nav__search">
        <img src="~/assets/img/person.png" alt="Личный кабинет" class="AppHeader-nav-person AppHeader-nav__person">
        <BurgerMenu />
        <HeaderDropdown :options="['RU','EN']" />
      </nav>
    </header>
</template>

<style lang="sass" scoped>
  @import "AppHeader"
</style>