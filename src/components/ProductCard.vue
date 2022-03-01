<template>
  <div class="card">
    <g-link :to="product.node.path">
    <div class="card-image">
      <figure class="image is-square">
        <img :src="`../../${product.node.image}`" />
      </figure>
    </div>
    <div class="card-content">
      <div class="media">
        <div class="media-content">
          <p class="title is-4">{{ product.node.name }}</p>
          <p class="subtitle is-6">{{ product.node.description }}</p>
        </div>
      </div>

      <div class="content">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit.
        Phasellus nec iaculis mauris. <a>@bulmaio</a>.
      </div>
    </div>
    </g-link>
  </div>
</template>

<script>
export default {
  props: { product: {} },
};
</script>