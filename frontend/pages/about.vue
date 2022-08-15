<template>
  <div>
    <Header :h1="title"/>
  <div class="container">
    <div class="row">
      <div class="col-lg-12">
                  <nav aria-label="breadcrumb" class="mt-4">
            <ol class="breadcrumb">
              <li class="breadcrumb-item"><a href="">Главная</a></li>
              <li class="breadcrumb-item active" aria-current="page">О проекте</li>
            </ol>
          </nav>
        <p></p>
        <p class="lead">Я люблю ораторское искусство и Павла Дурова.</p>
        <p class ="lead">Недавно узнал о том, что Дуров в своё время собрал речи исторических деятелей на своём сайте durov.com. И я захотел послушать. Но всё, что я нашёл — список речей, которые публиковал Дуров, и снэпшоты сайта на Wayback Machine</p>
        <img src="img/snapshot.png" class = "img-fluid w-65">
        <p class="lead">Поэтому я решил восстановить «самую большую в российской сети коллекцию речей». Чтобы и у вас, и у меня была возможность слушать лучших ораторов человечества: учиться у них вербальным и невербальным приёмам и прокачивать навык публичных выступлений. Присоединяйтесь.</p>
        
      </div>
    </div>
  </div>
  </div>
</template>

<script>
import Header from "@/components/Header";
export default {
  components: {Header},
  layout: "post_detail",
  name: "success",
  data() {
    return {
      title: "О проекте"
    }
  }
}
</script>

<style scoped>

</style>