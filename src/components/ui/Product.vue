<template>
    <div class="card">
        <div class="card-image">
            <img :src="image" alt="">
        </div>
        <div class="card-content">
            <p class="card-title">{{ title }}</p>
            <div class="info">
                <p class="card-price">{{ price }}$</p>
                <p class="card-size">{{ size }} см</p>
            </div>
            <Button theme="full" text="Подробнее" icon="/src/assets/images/arrow.png" class="product-button"/>
        </div>
    </div>
</template>

<script>
import Button from '@/components/ui/Button.vue'

export default {
  components: {
    Button
  },
  props: {
    title: {
      type: String,
      default: 'Кулинарная гладь'
    },
    price: {
      type: [String, Number],
      default: '11,4'
    },
    size: {
      type: [String, Number],
      default: '180'
    },
    image: {
      type: String,
      default: '/src/assets/images/blue.png'
    }
  }
}
</script>

<style scoped>
.card {
    width: 260px;
    height: 431px;
    background: white;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 4px 10px rgba(0,0,0,0.1);
}

.card-image {
    width: 100%;
    height: 260px;
}

.card-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.card-content {
    padding: 15px;
}

.card-title {
    font-size: var(--text-lg);
    font-weight: 600;
    margin-bottom: 8px;
    font-family: var(--font-family);
}

.card-price {
    font-size: var(--text-xl);
    font-weight: 600;
    font-family: var(--font-family);
}

.card-size {
    font-size: var(--text-sm);
    color: var(--size-color);
    margin-top: 25px;
    font-family: var(--font-family);
}

.info{
    display: flex;
    flex-wrap: nowrap;
    gap: 15px;
    margin-top: -20px;
}

.product-button{
    width: 220px;
    height: 55px;
    margin-left: 1px;
    justify-content: space-between;
    padding-left: 20px;
    padding-right: 30px;

}

</style>