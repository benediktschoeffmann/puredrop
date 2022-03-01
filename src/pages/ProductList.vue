<template>  
    <Layout pageTitle="Pure Drop" pageSubtitle="Product Site">
      <div class="section">
        <div class="container">
          <div class="columns">
            <div class="column"></div>
            <div class="column cards-grid is-four-fifths">
              <article class="card grid-item" v-for="product in $page.products.edges" :key="product.id">
                <ProductCard :product="product"/>
              </article>
            </div>
            <div class="column"></div>
          </div>
        </div>
      </div>
    </Layout>
</template>

<page-query>
query {
 products: allProduct {
    totalCount
    edges {
      node {
        id
        path
        price
        name
        date
        description
        image 
        content
      }
    }
  }
}
</page-query>

<script>
import ProductCard from '../components/ProductCard'
export default {
    components: { ProductCard },
};
</script>

<style>

</style>