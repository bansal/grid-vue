<template>
    <div class="card" :style="`background-image:url(${image})`">
        <div class="card-body">
            <slot></slot>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    image: String,
  }
}
</script>