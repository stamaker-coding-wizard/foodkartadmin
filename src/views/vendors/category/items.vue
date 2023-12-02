<template>
  <div class="main-content">
      <breadcumb :page="'Business Items'" :folder="'Business'" :folder2="'Items'" />
      
      <b-row>
          <!-- ICON BG -->
    
          <b-col lg="3" md="6" sm="12">
            <b-card
              class="card-icon-bg card-icon-bg-primary o-hidden mb-30 text-center"
            >
              <i class="i-Add-User"></i>
              <div class="content">
                <p class="text-muted mt-2 mb-0">New Leads</p>
                <p class="text-primary text-24 line-height-1 mb-2">205</p>
              </div>
            </b-card>
          </b-col>
          <b-col lg="3" md="6" sm="12">
            <b-card
              class="card-icon-bg card-icon-bg-primary o-hidden mb-30 text-center"
            >
              <i class="i-Financial"></i>
              <div class="content">
                <p class="text-muted mt-2 mb-0">Sales</p>
                <p class="text-primary text-24 line-height-1 mb-2">4021</p>
              </div>
            </b-card>
          </b-col>
          <b-col lg="3" md="6" sm="12">
            <b-card
              class="card-icon-bg card-icon-bg-primary o-hidden mb-30 text-center"
            >
              <i class="i-Checkout-Basket"></i>
              <div class="content">
                <p class="text-muted mt-2 mb-0">Orders</p>
                <p class="text-primary text-24 line-height-1 mb-2">80</p>
              </div>
            </b-card>
          </b-col>
          <b-col lg="3" md="6" sm="12">
            <b-card
              class="card-icon-bg card-icon-bg-primary o-hidden mb-30 text-center"
            >
              <i class="i-Money-2"></i>
              <div class="content">
                <p class="text-muted mt-2 mb-0">Expense</p>
                <p class="text-primary text-24 line-height-1 mb-2">1200</p>
              </div>
            </b-card>
          </b-col>
      </b-row>

      <div class="row">
          
          <b-col md="12">
              
              <b-card  
                  >
                  
                  <b-tabs  
                  active-nav-item-class="nav nav-tabs"
                  content-class=""
                  >
                      
                      <b-tab title="Food" active>
                        <!--
                          <div class="col-md-12 mb-3">        
                              <div class="table-responsive">
                                  <table class="table">
                                      <tbody>
                                          <tr v-for="(food, index) in foods" :key="food.id">
                                              <th scope="row">{{ index + 1 }}</th>
                                              <td class="d-md-flex">
                                                <div class="flex-column" style="margin-right: 1rem;">
                                                 
                                                  
                                                  <img :src="food.Url" style="width:120px;hight:120px; border-radius:50%;">
                                                </div>
                                                <div class="flex-column">
                                                  
                                                  <h4>{{ food.name }}</h4>
                                                  <p><span class="text-info">Vendor:</span> <span class="text-success">{{ food.vendor}}</span></p>
                                                  
                                                </div>
                                              </td>

                                              <td class="text-right">
                                                  
                                              </td>
                                              
                                              <td class="text-right">
                                                  <h2> {{ food.price }}</h2>
                                                  <span>{{ food.status }}</span>
                                              </td>
                                              
                                              <td>
                          
                                                <a class="text-success mr-2" @click="editRow(index)" style="cursor:pointer;"><i class="nav-icon i-Pen-2 font-weight-bold"></i></a>
                      
                                                <a class="text-danger mr-2" @click="deleteRow(index)" style="cursor:pointer;"><i class="nav-icon i-Close-Window font-weight-bold"></i></a>
                                              </td>
                                          </tr>

                                          
                                      </tbody>
                                  </table>
                              </div>      
                          </div>-->
                          <Foods/>
                        </b-tab>
                      <b-tab title="Groceries">
                          <groceries/>
                      </b-tab>
                      <b-tab title="Drinks">
                        <Drinks/>
                    </b-tab>
                      
                  </b-tabs>         
              </b-card>      
          </b-col>

          
          
      </div>

      

  </div>
</template>

<script>
import Foods from "./Component/ItemsOrder/Food.vue";
import groceries from "./Component/ItemsOrder/groceries.vue";
import Drinks from "./Component/ItemsOrder/Drinks.vue";

export default {

  components: {
    // Register Bootstrap-Vue components
    
    Foods,
    groceries,
    Drinks,
    
  },
  
  
  
};
</script>
<style scoped>
.custom-dropdown {
  position: relative;
  display: inline-block;
}

.selected-option {
  cursor: pointer;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

.dropdown-options {
  display: none;
  position: absolute;
  top: 100%;
  left: 0;
  background-color: #fff;
  border: 1px solid #ccc;
  border-top: none;
  border-radius: 0 0 4px 4px;
}

.dropdown-options div {
  padding: 10px;
}

.dropdown-options div:hover {
  background-color: #f2f2f2;
}

</style>
