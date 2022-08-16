<template>
  <!--Product-->
  <div class="product">
      <div class="product-header">
          <h1 class="text-center">Product Management</h1>
          <router-link to="/product/create">Add New</router-link>
      </div>

      <div class="product-content">
        <table class="table table-bordered">
              <thead>
                  <tr>
                    <th class="text-center" scope="col">Number Order</th>
                    <th class="text-center" scope="col">Product Name</th>
                    <th class="text-center" scope="col">Price</th>
                    <th class="text-center" scope="col">Handle</th>
                  </tr>
              </thead>
              <tbody>
                <tr>
                  <th class="text-center" scope="row">1</th>
                  <td>Mark</td>
                  <td>Otto</td>
                  <td>@mdo</td>
                </tr>
                <tr>
                  <th class="text-center" scope="row">2</th>
                  <td>Jacob</td>
                  <td>Thornton</td>
                  <td>@fat</td>
                </tr>
              <tr>
                  <th class="text-center" scope="row">3</th>
                  <td>Jacob</td>
                  <td>Thornton</td>
                  <td>@fat</td>
                </tr>
              </tbody>
        </table>
      </div>
  </div>
</template>

<script>
export default {
    name: 'List-Product'
}
</script>

<style scoped>

.product-header {
  margin: 60px 0;
}
.product-content {
  width: 60%;
  margin: auto;
}
</style>