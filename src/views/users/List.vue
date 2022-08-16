<template>
  <!--Product-->
  <div class="product">
      <div class="product-header">
          <h1 class="text-center">User Management</h1>
          <router-link to="/user/create">Add New</router-link>
      </div>

      <div class="product-content">
        <table class="table table-bordered">
              <thead>
                  <tr>
                    <th class="text-center" scope="col">Number</th>
                    <th class="text-center" scope="col">Name</th>
                    <th class="text-center" scope="col">Email</th>
                    <th class="text-center" scope="col">Address</th>
                  </tr>
              </thead>
              <tbody>
                <tr>
                  <th class="text-center" scope="row">1</th>
                  <td></td>
                  <td></td>
                  <td></td>
                </tr>
                <tr>
                  <th class="text-center" scope="row">2</th>
                  <td></td>
                  <td></td>
                  <td></td>
                </tr>
              <tr>
                  <th class="text-center" scope="row">3</th>
                  <td></td>
                  <td></td>
                  <td></td>
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