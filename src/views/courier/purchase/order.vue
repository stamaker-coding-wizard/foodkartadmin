<template>
    <div class="main-content">
        
        <breadcumb :page="'Revenue Orders'" :folder="'Revenue'" :folder2="'Order'" />
       

       

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
                  <p class="text-primary text-24 line-height-1 mb-2">$4021</p>
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
                  <p class="text-primary text-24 line-height-1 mb-2">$1200</p>
                </div>
              </b-card>
            </b-col>
        </b-row>

        <div class="row">
            <div class="col-md-12 mb-3"> 
              <orderTable/>
          </div>
        </div>


    </div>
</template>

<script>
import orderTable from './orderTable/orderT.vue'
export default {
    components: {
        orderTable,
    }
}
</script>



<style>
.dropdown {
  position: relative;
  display: inline-block;
}

.dropbtn {
  background-color: #3498db;
  color: white;
  padding: 10px;
  border: none;
}

.dropdown-content {
  display: none;
  position: absolute;
  background-color: #f1f1f1;
  min-width: 160px;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
}

.dropdown-content button {
  background-color: #ddd;
  color: black;
  padding: 12px 16px;
  border: none;
  width: 100%;
  text-align: left;
}

.dropdown-content button:hover {
  background-color: #f2f2f2;
}

.dropdown:hover .dropdown-content {
  display: block;
}

.dropdown:hover .dropbtn {
  background-color: #2980B9;
}
.img{
    width: 80px;
    height: 80px;
    object-fit: cover;
    border-radius: 50%;
}
</style>