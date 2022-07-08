<template>
    <div :class="`grid-item size-${item.size}`">
        <Card :image="item.image">
                <div class="wrapper">
                    <span class="country">{{item.country}}</span>
                    <h3 class="city">{{item.city}}</h3>
                    <div class="details">
                        <p class="summary">{{item.summary}}</p>
                        <button class="button">Explore More</button>
                    </div>
                </div>
        </Card>
    </div>
</template>

<script>
import Card from './Card.vue';

export default {
  name: 'GridItem',
  components:{
    Card,
  },
  props: {
    item: Object,
  }
}
</script>
<style scoped>
.grid-item{
    height: 400px;
}

.wrapper{
    max-height: 100%;
    cursor: pointer;
    position: relative;
    transition: all .5s ease;
}

.country {
    font-size: 0.8rem;
    color: rgba(255, 255, 255, 0.5);
    text-transform: uppercase;
    letter-spacing: 0.3rem;
}

.city {
    font-size: 1.8rem;
    color: rgba(255, 255, 255);
    text-transform: uppercase;
    font-weight: 500;
}

.summary{
    color: rgba(255, 255, 255, 0.9);
    margin: 2rem 1rem;
    text-align: center;
    font-weight: 300;
    font-size: 0.9rem;
    line-height: 1.5;
}

.button{
    display: inline-block;
    padding: 0.8rem 1.6rem;
    margin-top: 1rem;
    border: 1px solid #ffffff;
    border-radius: 0.3rem;
    color: #ffffff;
    background-color: rgba(255, 255, 255, 0.1);
    font-size: 0.8rem;
    text-decoration: none;
    cursor: pointer;
    transition: all .5s ease;
}
.button:hover{
    background-color: rgba(255, 255, 255, 0.9);
    color: #000000;
}
.details{
    transform: scale(0);
    height: 0;
    overflow: hidden;
    transition: all .5s ease;
}

.card:hover .details{
    transform: scale(1);
    height: auto;
}
</style>