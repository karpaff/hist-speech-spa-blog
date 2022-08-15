<template>
  <div class="container-fluid home-slider">
    <div id="carouselExampleCaptions" class="carousel slide" data-ride="carousel">
      <ol class="carousel-indicators">
        <li data-target="#carouselExampleCaptions" data-slide-to="0" class="active"></li>
        <li data-target="#carouselExampleCaptions" data-slide-to="1"></li>
        <li data-target="#carouselExampleCaptions" data-slide-to="2"></li>
      </ol>
      <div class="carousel-inner">
        <nuxt-link :to="'/tags/mlk'" class="carousel-item active">
          <img src="/img/first_img.png" class="d-block w-100" alt="Первая картинка">
          <div class="carousel-caption d-none d-md-block" style = "text-shadow: black 2px 1px 1px; color: white;">
            <h5>Речи Мартина Лютера Кинга</h5>
            <p>Самого известного американского оратора XX века.</p>
          </div>
        </nuxt-link>
        <nuxt-link :to="'/tags/lenin'" class="carousel-item">
          <img src="/img/second_img.png" class="d-block w-100" alt="Вторая картинка">
          <div class="carousel-caption d-none d-md-block" style = "text-shadow: black 2px 1px 1px; color: white;">
            <h5>Речи Владимира Ильича Ленина</h5>
            <p>Российского революционера и государственного деятеля начала XX века.</p>
          </div>
        </nuxt-link>
        <nuxt-link :to="'/tags/reagan'" class="carousel-item">
          <img src="/img/third_img.png" class="d-block w-100" alt="Третья картинка">
          <div class="carousel-caption d-none d-md-block" style = "text-shadow: black 2px 1px 1px; color: white;">
            <h5>Речи Рональда Уилсона Рейгана</h5>
            <p>40-го Президента США, киноактера и радиоведущего.</p>
          </div>
        </nuxt-link>
      </div>
      <a class="carousel-control-prev" href="#carouselExampleCaptions" role="button" data-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
      </a>
      <a class="carousel-control-next" href="#carouselExampleCaptions" role="button" data-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "Slider"
}
</script>

<style scoped>

</style>