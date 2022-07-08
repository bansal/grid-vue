<template>
    <div class="banner">
        <Card :image="image">
            <span class="title">{{title}}</span>
            <h1 class="heading">{{heading}}</h1>
            <p class="summary">{{summary}}</p>
        </Card>
    </div>
</template>

<script>
import Card from './Card.vue';

export default {
  name: 'Banner',
  components:{
    Card
  },
  props: {
    image: String,
    title: String,
    heading: String,
    summary: String,
  }
}
</script>
<style>
.banner{
    margin-bottom: 1rem;
    height: 500px;
}
.title{
    font-size: 0.8rem;
    color: rgba(255, 255, 255, 0.5);
    text-transform: uppercase;
    letter-spacing: 0.3rem;
}
.heading{
    font-size: 3.5rem;
    color: #ffffff;
    margin-top: 1rem;
}
.summary{
    color: rgba(255, 255, 255, 0.9);
    margin-top: 1rem;
    text-align: center;
    font-weight: 300;
    font-size: 1.2rem;
    line-height: 1.5;
}
</style>