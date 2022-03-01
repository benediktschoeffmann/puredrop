<template>  
    <Layout pageTitle="Pure Drop" pageSubtitle="Product Site">
      <div class="section">
        <div class="container">
          <div class="columns">
            <div class="column"></div>
            <div class="column cards-grid is-four-fifths">
              <article class="card grid-item" v-for="edge in $page.products.edges" :key="edge.node.id">
                <div class="card">
                  <g-link :to="edge.node.path">
                    <div class="card-image">
                      <figure class="image is-1by1">
                        <img 
                          :src="`../../${edge.node.image}`"
                          :alt="`${edge.node.name} image`"
                        />
                      </figure>
                    </div>
                    <div class="card-content">
                      <div class="media">
                        <div class="media-content">
                          <p class="title is-4">{{ edge.node.name }}</p>
                          <p class="subtitle is-6">{{ edge.node.description }}</p>
                          <div class="level">
                            <div class="level-right">
                              <div class="level-item">
                                {{ edge.node.price }} € 
                              </div> 
                            </div>
                          </div>

                        </div>
                      
                      </div>
                    </div>
                    
                    
                  
                  </g-link>
                </div>

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
</script>

<style>
.card {
  margin-bottom: 15px;
  padding: 5px;
}

.card-image {
  width: 300px;
}
</style>