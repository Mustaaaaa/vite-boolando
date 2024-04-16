<template>
  <main>
    <section class="section">
      <div class="container">
        <div class="flex row">
          <div class="col-3" v-for="product in store.products">
            <div class="card">
              <div class="card-image">
                <img :src="'/' + product.frontImage" alt="">
                <span class="heart-icon" :class="{ 'red': product.isInFavorites }">&hearts;</span>
                <span  class="badge" v-for="badge in product.badges" :class="badge.type">{{ badge.value }}</span>
                <div class="overlay">
                  <img :src="'/' + product.backImage" alt="">
                </div>
              </div>
              <div>
                <p>{{ product.brand }}</p>
                <h4>{{ product.name }}</h4>
                <p>
                  <span class="red">{{ product.price }}&euro; </span>
                  <span class="line-throught">29,99&euro;</span>
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import store from '../store.js'
export default {
  data() {
    return {
      store: store,
    }
  }
}
</script>

<style lang="scss">
.card-image {
  position: relative;
}

.card-image>img {
  display: block;
}

.badge {
  line-height: 20px;
  color: white;
  font-size: 10px;
  padding: 0 5px;
}

.card {
  padding: 15px;
}

.card-image .badge {
  position: absolute;
  bottom: 35px;
  z-index: 10;
}

.card-image .tag {
  left: 40px;
  background-color: green;
}
.card-image .discount {
  left: 0px;
  background-color: red;
}

.heart-icon {
  position: absolute;
  right: 0px;
  top: 10px;
  z-index: 10;
  line-height: 35px;
  padding: 0 8px;
  font-size: 28px;
  background-color: white;
}

.card-image .overlay {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  opacity: 0;
  transition: none;
}

.card:hover .overlay {
  opacity: 1;
}

</style>