<script setup>
const props = defineProps({
  name: {
    type: String,
    required: true
  },
  price: {
    type: Number,
    required: true
  },
  inStock: {
    type: Boolean,
    default: true
  }
})

const emit = defineEmits(['addedToCart'])

function addToCart() {
  emit('addedToCart', props.name)
}
</script>

<template>
  <div class="card">
    <h3>{{ name }}</h3>

    <p>$ {{ price }}</p>

    <span v-if="inStock">
      ✅ In Stock
    </span>

    <span v-else>
      ❌ Out of Stock
    </span>

    <br><br>

    <button @click="addToCart">
      Add To Cart
    </button>
  </div>
</template>

<style scoped>
.card{
  border:1px solid #ddd;
  padding:15px;
  margin:10px;
}
</style>