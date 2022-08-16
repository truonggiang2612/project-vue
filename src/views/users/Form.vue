<template>
  <div class="product-create">
        <!--Header-->
        <div class="form-header">
            <h1 class="text-center">User Infomation</h1>
            <router-link class="router-link" to="/user">Back</router-link>
        </div>

        <!--Form-->
        <form class="form-info">
                <div class="form-input form-outline mb-4">
                    <label class="form-label">User Name:</label>
                    <input type="text"  class="form-control" placeholder="Enter user name..." />
                </div>


                <div class="form-input form-outline mb-4">
                    <label class="form-label">Password:</label>
                    <input type="password"  class="form-control" placeholder="Enter password..." />
                </div>

                <div class="form-input form-outline mb-4">
                    <label class="form-label ">Confirm Password:</label>
                    <input type="password"  class="form-control" placeholder="Confirm password..." />
                </div>

                <div class="form-input form-outline mb-4">
                    <label class="form-label ">Email address:</label>
                    <input type="text"  class="form-control" placeholder="Enter email..." />
                </div>

                <button type="submit" class="btn_handle btn-save">Signup</button>
                <button type="submit" class="btn_handle btn-cancel">Cancel</button>
        </form>
  </div>
</template>

<script>
export default {
    name: 'Form-Product'
}
</script>

<style scoped>
.product-create {
    border: 1px solid #ccc;
    width: 60%;
    margin: 60px auto;
    border-radius: 20px;
    background-image: url('https://digitalfuture.vn/wp-content/uploads/2022/03/Xem-123-Hinh-anh-hoa-dep-den-THUC-TINH-THI.jpg')
}

/* Header */
.form-header {
    margin: 60px 0;
}
.text-center {
    font-size: 52px;
    font-weight: 600;
    letter-spacing: 2px;
    text-shadow: 4px 4px rgb(41, 25, 252);
    color: #f3c137;;
}

.router-link {
    color: white;
    font-size: 20px;
    transition: 0.4s;
}
.router-link:hover {
    color: #f3c137;
}


/* Form */

.form-input {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 20px;
    margin: 40px 0;
}
.form-input input {
    width: 50%;
    height: 40px;
}

.form-label {
    color: white;
    font-size: 16px;
    width: 150px;
    height: 40px;
    line-height: 40px;
}

/* Button handle */
.btn_handle {
    width: 80px;
    height: 42px;
    border-radius: 10px;
    margin: 0 10px;
    border: none;
    margin-bottom: 20px;
}

.btn-save,
.btn-cancel {
    background-color: #4a4af0;
    color: white;
    font-size: 18px;
}

.btn-cancel {
    background-color: rgb(194, 41, 41);
}
</style>