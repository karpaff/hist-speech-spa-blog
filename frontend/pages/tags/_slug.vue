<template>
  <div>
    <Header :h1=title />
      <div class="container">
        <p class="my-3">Другие темы:
          <nuxt-link :to="`/tags/${tag.slug}`" class="badge badge-success mr-1" v-for="tag in tags" :key="name">{{tag.name}} </nuxt-link>
        </p>
        <div class="row">
          <div v-for="post in posts" :key="post.slug" class="col-md-4">
          <nuxt-link :to="`/posts/${post.slug}`" style = "text-decoration: none; color: black;" class="card mb-4 shadow-sm" >
              <img :src="post.image" alt="" class="card-img-top">
              <div class="card-body">
                <h4 class="card-title">{{ post.h1 }}</h4>
                <div v-html="post.description" class="truncate"></div>
                <div class="mb-2">
              <span v-for="tag in post.tags">
                <nuxt-link :to="`/tags/${tag.slug}`" class="mr-1 badge badge-info">{{ tag.name }}</nuxt-link>
              </span>
                </div>
                <div class="d-flex justify-content-between align-items-center">
                  <small class="text-muted">{{ post.created_at }}</small>
                </div>
              </div>
            </nuxt-link>
          </div>
        </div>
      </div>
  </div>
</template>

<script>
import axios from "axios";
import Header from "@/components/Header";


export default {
  components: {Header},
  layout: "post_detail",
  async asyncData({params}) {
    const { data } = await axios.get(`http://127.0.0.1:8000/api/tags/${params.slug}`);
    const tags = await axios.get(`http://127.0.0.1:8000/api/tags/`)

    let result = tags.data.filter(obj => {
      return obj.slug === params.slug
    })
    return {
      posts: data.results,
      title: `${result[0].name}`,
      tags: tags.data,
    }
  },
}
</script>

<style scoped>

</style>