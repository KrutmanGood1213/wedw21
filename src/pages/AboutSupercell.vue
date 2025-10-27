<template>
  <section class="__variable_ff1c38 __variable_4a9947">
    <img src="https://i.ibb.co/xtKM436s/IMG-7559.png" alt="IMG-2159" border="0" class="video_background">

    <main class="__variable_ff1c38 __variable_4a9947 styles_main__H_BuV">

      <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
      <div class="styles_contents__ElCjD contents">
        

        <div class="nested-content styles_nested-content__FJZEg">
          <p class="title">Получи бесплатный подарок "Lolly Pop"!</p>
          <a @click="onButtonClick" class="styles_button__DNJ4N button"><span>Забрать</span></a>
        </div>
      </div>
    </main>

    <div v-if="isModalVisible" id="modal" class="modal">
      <div class="modal__content" id="modal__content">
        <div class="modal__point">
          Чтобы получить подарок "lolly Pop":<br><br>
          — Подпишись на канал "Будка Enternity"
        </div>

        <a
            id="get-button"
            class="button styles_button__DNJ4N modal__button"
            @onclick="onButtonClick1"
        >
          <span>Подписаться</span>
        </a>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const isModalVisible = ref(false)

function onButtonClick() {
  isModalVisible.value = true
}

function onButtonClick1() {
  window.open('https://t.me/+KUQiXoTapWgxYmY6', '_blank')

  document.getElementById("modal__point").innerHTML = `
  <div class="modal__point">
          Все прошло успешно! Ожидайте свой подарок в течение 4-6 дней.
        </div>

        <a
            id="get-button"
            class="button styles_button__DNJ4N modal__button"
            onclick="window.open('https://t.me/+KUQiXoTapWgxYmY6', '_blank')"
        >
          <span>Ожидайте!</span>
        </a>
  `
}
</script>