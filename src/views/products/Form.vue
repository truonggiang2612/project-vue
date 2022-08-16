<template>
  <div class="product-create">
        <!--Header-->
        <div class="form-header">
            <h1 class="text-center">Product Infomation</h1>
            <router-link to="/product">Back</router-link>
        </div>

        <!--Form-->
        <form @submit.prevent="save()" class="form-info">

            <div class="form-input form-outline mb-4">
                <label class="form-label">Product Name:</label>
                <input 
                    type="text"
                    class="form-control"
                    v-model="product.name"
                    v-bind:class="{'is-invalid': errs.name}"
                    @input="validate"
                    @blur="validate"/>
                <div class="show-err">{{ errs.name }}</div>
            </div>


            <div class="form-input form-outline mb-4">
                <label class="form-label">Product price:</label>
                <input
                    type="text"
                    class="form-control"
                    v-model="product.price"
                    v-bind:class="{'is-invalid': errs.price}"
                    @input="validate"
                    @blur="validate"/>
                <div class="show-err">{{ errs.price }}</div>
            </div>

            <div class="form-input form-outline mb-4">
                <label class="form-label ">Description:</label>
                <input 
                    type="text"  
                    class="form-control description" 
                    v-model="product.description"
                    v-bind:class="{'is-invalid': errs.description}" 
                    @input="validate"
                    @blur="validate"
                    />
                <div class="show-err">{{ errs.description }}</div>
            </div>

           
            <!-- Submit button -->
            <button type="submit" class="btn_handle btn-save">Save</button>
            <button @click="setupForm" type="submit" class="btn_handle btn-cancel">Cancel</button>
        </form>
  </div>
</template>

<script>

export default {
    name: 'Form-Product',
    data() {
        return {
            product: {
                name:'',
                price:'',
                description:''
            },

            errs: {
                name:'',
                price:'',
                description:''
            }
        }
    },

    methods: {
        validate() {
            this.errs = {
                name:'',
                price:'',
                description:''
            }
            if(!this.product.name) {
                this.errs.name = '=> Name field is required!'
            }

            if(!this.product.price) {
                this.errs.price = '=> Price field is required!'
            } else if(!this.checkPrice(this.product.price))
                this.errs.price = '=> Price must be a number'

            if(!this.product.description) {
                this.errs.description = '=> Description is catch!'
            }
            
        },

        checkPrice(value) {
            return /^\d*$/.test(value)
        },

        save() {
            console.log('save');
            this.validate()
        },

        setupForm() {
            console.log('set up');
        }

    }
}
</script>

<style scoped>
.product-create {
    width: 60%;
    margin: 60px auto;
}

/* Header */
.form-header {
    margin: 60px 0;
}

/* Form */
.form-info {
    border: 1px solid #ccc;
    border-radius: 20px;
}

.form-input {
    display: flex;
    gap: 20px;
    margin: 40px 0;
}
.form-input input {
    width: 60%;
    height: 40px;
}

.form-input .description {
    height: 100px;
}

.form-label {
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

.is-invalid {
    border: 1px solid red;
    box-shadow: 2px 2px 2px red;
    opacity: 0.6;
}
.show-err {
    color: red;
    font-size: 18px;
    line-height: 40px;
}
</style>