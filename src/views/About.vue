<template>
  <div class="about">

    <!-- Breadcrumb -->
    <section class="gs-container gs-container_center">
      <ol class="gs-breadcrumb">
        <li class="gs-breadcrumb__list-item"> <router-link class="gs-breadcrumb__link" :to="{ name: 'Home' }"> GS Гусев </router-link> </li>
        <li class="gs-breadcrumb__list-item gs-breadcrumb__list-item_active"> О нас </li>
      </ol>
    </section>

    <section class="gs-container gs-container_center">
      <div class="gs-well">
        Наша команда:
        <ol> 
          <li>
            Вадим Канинский - <a href="https://github.com/vadimcpp"> GitHub </a>
          </li>
          <li>
            Ярослав Карас - <a href="https://github.com/yarkaras"> GitHub </a>
          </li>
          <li>
            Листопад Евгений - <a href="https://github.com/gutal1n"> GitHub </a>
          </li>
          <li>
            Акимова Дарья - <a href="https://github.com/DaryaAkimova"> GitHub </a>
          </li>
        </ol>
      </div>
    </section>
    
    <section class="gs-container gs-container_center">
      <div class="gs-well gs-well_text-center">
        <p> Плохо работает сайт? <br> <a href="https://vk.com/vadimcpp"> Напишите программисту </a> </p>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'About',
  props: ['title'],
  created () {
    document.title = this.title
  },
  watch: {
    title () {
      // only used when the title changes after page load
      document.title = this.title
    }
  }
}
</script>

<style lang="scss" scoped>

@import '../assets/scss/about.scss';

@keyframes slideOutRight {
  from {
    transform: translate3d(0, 0, 0);
  }

  to {
    visibility: hidden;
    transform: translate3d(100%, 0, 0);
  }
}

@keyframes slideInRight {
  from {
    transform: translate3d(100%, 0, 0);
    visibility: visible;
  }

  to {
    transform: translate3d(0, 0, 0);
  }
}

.slide-enter {
  opacity: 0;
}

.slide-enter-active {
  animation-name: slideInRight;
  animation-duration: 1s;
  animation-fill-mode: both;
}

</style>
