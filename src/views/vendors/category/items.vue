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
                          <div class="col-md-12 mb-3">        
                              <div class="table-responsive">
                                  <table class="table">
                                      <tbody>
                                          <tr>
                                              <td class="d-md-flex">
                                                  <div class="flex-column" style="margin-right: 1rem;">
                                                    <!-- Content for the first column -->
                                                    <img src="@/assets/images/mac_book.jpg" alt="Hello" style="width:150px;hight:150px;">
                                                  </div>
                                                  <div class="flex-column">
                                                    <!-- Content for the second column -->
                                                    <h4>Great Logo Design</h4>
                                                    <p class="text-success">UI lib admin themes</p>
                                                    <div class="d-flex">
                                                      
                                                      <p>Author: <span class="text-info">John snow</span></p>
                                                      <p class="ml-3">Released:<span class="text-info">22.08.17</span></p>
                                                      
                                                    </div>
                                                  </div>
                                              </td>

                                              <td class="text-right">
                                                  
                                              </td>
                                              
                                              <td class="text-right">
                                                  <h2>19,200</h2>
                                                  <span>sales</span>
                                              </td>
                                              
                                              <td><a class="text-success mr-2" href="#"><i class="nav-icon i-Pen-2 font-weight-bold"></i></a><a class="text-danger mr-2" href="#"><i class="nav-icon i-Close-Window font-weight-bold"></i></a></td>
                                          </tr>
                                          <tr>
                                              <td class="d-md-flex">
                                                  <div class="flex-column" style="margin-right: 1rem;">
                                                    <!-- Content for the first column -->
                                                    <img src="@/assets/images/mac_book.jpg" alt="Hello" style="width:150px;hight:150px;">
                                                  </div>
                                                  <div class="flex-column">
                                                    <!-- Content for the second column -->
                                                    <h4>Great Logo Design</h4>
                                                    <p class="text-success">UI lib admin themes</p>
                                                    <div class="d-flex">
                                                      
                                                      <p>Author: <span class="text-info">John snow</span></p>
                                                      <p class="ml-3">Released:<span class="text-info">22.08.17</span></p>
                                                      
                                                    </div>
                                                  </div>
                                              </td>

                                              <td class="text-right">
                                                  
                                              </td>
                                              
                                              <td class="text-right">
                                                  <h2>29,200</h2>
                                                  <span>sales</span>
                                              </td>
                                              
                                              <td><a class="text-success mr-2" href="#"><i class="nav-icon i-Pen-2 font-weight-bold"></i></a><a class="text-danger mr-2" href="#"><i class="nav-icon i-Close-Window font-weight-bold"></i></a></td>
                                          </tr>
                                          <tr>
                                              <td class="d-md-flex">
                                                  <div class="flex-column" style="margin-right: 1rem;">
                                                    <!-- Content for the first column -->
                                                    <img src="@/assets/images/mac_book.jpg" alt="Hello" style="width:150px;hight:150px;">
                                                  </div>
                                                  <div class="flex-column">
                                                    <!-- Content for the second column -->
                                                    <h4>Great Logo Design</h4>
                                                    <p class="text-success">UI lib admin themes</p>
                                                    <div class="d-flex">
                                                      
                                                      <p>Author: <span class="text-info">John snow</span></p>
                                                      <p class="ml-3">Released:<span class="text-info">22.08.17</span></p>
                                                      
                                                    </div>
                                                  </div>
                                              </td>

                                              <td class="text-right">
                                                  <h2>23,200</h2>
                                                  <span>Quality</span>
                                              </td>
                                              
                                              <td class="text-right">
                                                  <h2>23,200</h2>
                                                  <span>sales</span>
                                              </td>
                                              
                                              <td><a class="text-success mr-2" href="#"><i class="nav-icon i-Pen-2 font-weight-bold"></i></a><a class="text-danger mr-2" href="#"><i class="nav-icon i-Close-Window font-weight-bold"></i></a></td>
                                          </tr>
                                      </tbody>
                                  </table>
                              </div>      
                          </div>
                      </b-tab>
                      <b-tab title="Groceries">
                          <div class="col-md-12 mb-3">        
                              <div class="table-responsive">
                                  <table class="table">
                                      <tbody>
                                          <tr>
                                              <td class="d-md-flex">
                                                  <div class="flex-column" style="margin-right: 1rem;">
                                                    <!-- Content for the first column -->
                                                    <img src="@/assets/images/mac_book.jpg" alt="Hello" style="width:150px;hight:150px;">
                                                  </div>
                                                  <div class="flex-column">
                                                    <!-- Content for the second column -->
                                                    <h4>Great Logo Design</h4>
                                                    <p class="text-success">UI lib admin themes</p>
                                                    <div class="d-flex">
                                                      
                                                      <p>Author: <span class="text-info">John snow</span></p>
                                                      <p class="ml-3">Released:<span class="text-info">22.08.17</span></p>
                                                      
                                                    </div>
                                                  </div>
                                              </td>

                                              <td class="text-right">
                                                  
                                              </td>
                                              
                                              <td class="text-right">
                                                  <h2>19,200</h2>
                                                  <span>sales</span>
                                              </td>
                                              
                                              <td><a class="text-success mr-2" href="#"><i class="nav-icon i-Pen-2 font-weight-bold"></i></a><a class="text-danger mr-2" href="#"><i class="nav-icon i-Close-Window font-weight-bold"></i></a></td>
                                          </tr>
                                          <tr>
                                              <td class="d-md-flex">
                                                  <div class="flex-column" style="margin-right: 1rem;">
                                                    <!-- Content for the first column -->
                                                    <img src="@/assets/images/mac_book.jpg" alt="Hello" style="width:150px;hight:150px;">
                                                  </div>
                                                  <div class="flex-column">
                                                    <!-- Content for the second column -->
                                                    <h4>Great Logo Design</h4>
                                                    <p class="text-success">UI lib admin themes</p>
                                                    <div class="d-flex">
                                                      
                                                      <p>Author: <span class="text-info">John snow</span></p>
                                                      <p class="ml-3">Released:<span class="text-info">22.08.17</span></p>
                                                      
                                                    </div>
                                                  </div>
                                              </td>

                                              <td class="text-right">
                                                  
                                              </td>
                                              
                                              <td class="text-right">
                                                  <h2>29,200</h2>
                                                  <span>sales</span>
                                              </td>
                                              
                                              <td><a class="text-success mr-2" href="#"><i class="nav-icon i-Pen-2 font-weight-bold"></i></a><a class="text-danger mr-2" href="#"><i class="nav-icon i-Close-Window font-weight-bold"></i></a></td>
                                          </tr>
                                          <tr>
                                              <td class="d-md-flex">
                                                  <div class="flex-column" style="margin-right: 1rem;">
                                                    <!-- Content for the first column -->
                                                    <img src="@/assets/images/mac_book.jpg" alt="Hello" style="width:150px;hight:150px;">
                                                  </div>
                                                  <div class="flex-column">
                                                    <!-- Content for the second column -->
                                                    <h4>Great Logo Design</h4>
                                                    <p class="text-success">UI lib admin themes</p>
                                                    <div class="d-flex">
                                                      
                                                      <p>Author: <span class="text-info">John snow</span></p>
                                                      <p class="ml-3">Released:<span class="text-info">22.08.17</span></p>
                                                      
                                                    </div>
                                                  </div>
                                              </td>

                                              <td class="text-right">
                                                  <h2>23,200</h2>
                                                  <span>Quality</span>
                                              </td>
                                              
                                              <td class="text-right">
                                                  <h2>23,200</h2>
                                                  <span>sales</span>
                                              </td>
                                              
                                              <td><a class="text-success mr-2" href="#"><i class="nav-icon i-Pen-2 font-weight-bold"></i></a><a class="text-danger mr-2" href="#"><i class="nav-icon i-Close-Window font-weight-bold"></i></a></td>
                                          </tr>
                                      </tbody>
                                  </table>
                              </div>      
                          </div>
                      </b-tab>
                      
                  </b-tabs>         
              </b-card>      
          </b-col>

          
          
      </div>
  </div>
</template>

<script>
export default {
     metaInfo: {
  // if no subcomponents specify a metaInfo.title, this title will be used
title: "items"
},
  data() {
    return {
      text: `
        Anim pariatur cliche reprehenderit, enim eiusmod high life accusamus terry
        richardson ad squid. 3 wolf moon officia aute, non cupidatat skateboard dolor
        brunch. Food truck quinoa nesciunt laborum eiusmod. Brunch 3 wolf moon
        tempor, sunt aliqua put a bird on it squid single-origin coffee nulla
        assumenda shoreditch et. Nihil anim keffiyeh helvetica, craft beer labore
        wes anderson cred nesciunt sapiente ea proident. Ad vegan excepteur butcher
        vice lomo. Leggings occaecat craft beer farm-to-table, raw denim aesthetic
        synth nesciunt you probably haven't heard of them accusamus labore VHS.
      `
    }
  }
}
</script>
<style scoped>
 
</style>
