<template>
    <div class="main-content">
        <breadcumb :page="'Business Items'" :folder="'Business'" :folder2="'Items'" />
        <!--
        <b-row>
            <b-col lg="6" md="6">
                <b-card title="Accordion Group" class="mb-30">
                    <div role="tablist">
                        <b-card no-body class="ul-card__border-radius">
                        <b-card-header header-tag="header" class="p-1"  role="tab">
                            <b-button class="card-title mb-0" block href="#" v-b-toggle.accordion-1 variant="transparent">Accordion 1</b-button>
                        </b-card-header>
                        <b-collapse id="accordion-1" visible accordion="my-accordion" role="tabpanel">
                            <b-card-body>
                            <b-card-text>I start opened because <code>visible</code> is <code>true</code></b-card-text>
                            <b-card-text>{{ text }}</b-card-text>
                            </b-card-body>
                        </b-collapse>
                        </b-card>

                        <b-card no-body class="ul-card__border-radius">
                        <b-card-header header-tag="header" class="p-1" role="tab">
                            <b-button  class="card-title mb-0" block href="#" v-b-toggle.accordion-2 variant="transparent">Accordion 2</b-button>
                        </b-card-header>
                        <b-collapse id="accordion-2" accordion="my-accordion" role="tabpanel">
                            <b-card-body>
                            <b-card-text>{{ text }}</b-card-text>
                            </b-card-body>
                        </b-collapse>
                        </b-card>

                        <b-card no-body class="ul-card__border-radius">
                        <b-card-header header-tag="header" class="p-1" role="tab">
                            <b-button class="card-title mb-0" block href="#" v-b-toggle.accordion-3 variant="transparent">Accordion 3</b-button>
                        </b-card-header>
                        <b-collapse id="accordion-3" accordion="my-accordion" role="tabpanel">
                            <b-card-body>
                            <b-card-text>{{ text }}</b-card-text>
                            </b-card-body>
                        </b-collapse>
                        </b-card>
                    </div>
                </b-card>
                <b-card title="Right control icon" class=" mb-30">
                    <div role="tablist">
                        <b-card no-body class="ul-card__border-radius">
                        <b-card-header header-tag="header" class="p-1"  role="tab">
                            <b-button class="card-title mb-0 custom_a" block href="#" v-b-toggle.accordion-4 variant="transparent">Accordion 1</b-button>
                        </b-card-header>
                        <b-collapse id="accordion-4" visible accordion="my-accordion" role="tabpanel">
                            <b-card-body>
                            <b-card-text>I start opened because <code>visible</code> is <code>true</code></b-card-text>
                            <b-card-text>{{ text }}</b-card-text>
                            </b-card-body>
                        </b-collapse>
                        </b-card>

                        <b-card no-body class="ul-card__border-radius">
                        <b-card-header header-tag="header" class="p-1" role="tab">
                            <b-button  class="card-title mb-0" block href="#" v-b-toggle.accordion-5 variant="transparent">Accordion 2</b-button>
                        </b-card-header>
                        <b-collapse id="accordion-5" accordion="my-accordion" role="tabpanel">
                            <b-card-body>
                            <b-card-text>{{ text }}</b-card-text>
                            </b-card-body>
                        </b-collapse>
                        </b-card>

                        <b-card no-body class="ul-card__border-radius">
                        <b-card-header header-tag="header" class="p-1" role="tab">
                            <b-button class="card-title mb-0" block href="#" v-b-toggle.accordion-6 variant="transparent">Accordion 3</b-button>
                        </b-card-header>
                        <b-collapse id="accordion-6" accordion="my-accordion" role="tabpanel">
                            <b-card-body>
                            <b-card-text>{{ text }}</b-card-text>
                            </b-card-body>
                        </b-collapse>
                        </b-card>
                    </div>
                </b-card>
            </b-col>
            <b-col lg="6" md="6">
                <b-card title="With Icons" class="mb-30">
                    <div role="tablist">
                        <b-card no-body class="ul-card__border-radius">
                        <b-card-header header-tag="header" class="p-1 header-elements-inline"  role="tab">
                            <b-button class="card-title mb-0 " block href="#" v-b-toggle.accordion-2-1 variant="transparent">
                               <span><i class="i-Big-Data text-18 font-weight-500 mr-1"> </i></span> Accordion 1</b-button>
                        </b-card-header>
                        <b-collapse id="accordion-2-1" visible accordion="my-accordion" role="tabpanel">
                            <b-card-body>
                            <b-card-text>I start opened because <code>visible</code> is <code>true</code></b-card-text>
                            <b-card-text>{{ text }}</b-card-text>
                            </b-card-body>
                        </b-collapse>
                        </b-card>

                        <b-card no-body class="ul-card__border-radius">
                        <b-card-header header-tag="header" class="p-1" role="tab">
                            <b-button  class="card-title mb-0" block href="#" v-b-toggle.accordion-2-2 variant="transparent">
                                <span><i class="i-Data-Settings text-18 font-weight-500 mr-1"> </i></span>
                                Accordion 2
                            </b-button>
                        </b-card-header>
                        <b-collapse id="accordion-2-2" accordion="my-accordion" role="tabpanel">
                            <b-card-body>
                            <b-card-text>{{ text }}</b-card-text>
                            </b-card-body>
                        </b-collapse>
                        </b-card>

                        <b-card no-body class="ul-card__border-radius">
                        <b-card-header header-tag="header" class="p-1" role="tab">
                            <b-button class="card-title mb-0" block href="#" v-b-toggle.accordion-2-3 variant="transparent">
                                 <span><i class="i-Bell1 text-18 font-weight-500 mr-1"> </i></span>
                                Accordion 3
                            </b-button>
                        </b-card-header>
                        <b-collapse id="accordion-2-3" accordion="my-accordion" role="tabpanel">
                            <b-card-body>
                            <b-card-text>{{ text }}</b-card-text>
                            </b-card-body>
                        </b-collapse>
                        </b-card>
                    </div>
                </b-card>

                <b-card title="Without Right Icons" class="mb-30">
                    <div role="tablist">
                        <b-card no-body class="ul-card__border-radius">
                        <b-card-header header-tag="header" class="p-1 header-elements-inline"  role="tab">
                            <b-button class="card-title mb-0 " block href="#" v-b-toggle.accordion-2-4 variant="transparent">
                               <span><i class="i-Big-Data text-18 font-weight-500 mr-1"> </i></span> Accordion 1</b-button>
                        </b-card-header>
                        <b-collapse id="accordion-2-4" visible accordion="my-accordion" role="tabpanel">
                            <b-card-body>
                            <b-card-text>I start opened because <code>visible</code> is <code>true</code></b-card-text>
                            <b-card-text>{{ text }}</b-card-text>
                            </b-card-body>
                        </b-collapse>
                        </b-card>

                        <b-card no-body class="ul-card__border-radius">
                        <b-card-header header-tag="header" class="p-1" role="tab">
                            <b-button  class="card-title mb-0" block href="#" v-b-toggle.accordion-2-5 variant="transparent">
                                <span><i class="i-Data-Settings text-18 font-weight-500 mr-1"> </i></span>
                                Accordion 2
                            </b-button>
                        </b-card-header>
                        <b-collapse id="accordion-2-5" accordion="my-accordion" role="tabpanel">
                            <b-card-body>
                            <b-card-text>{{ text }}</b-card-text>
                            </b-card-body>
                        </b-collapse>
                        </b-card>

                        <b-card no-body class="ul-card__border-radius">
                        <b-card-header header-tag="header" class="p-1" role="tab">
                            <b-button class="card-title mb-0" block href="#" v-b-toggle.accordion-2-6 variant="transparent">
                                 <span><i class="i-Bell1 text-18 font-weight-500 mr-1"> </i></span>
                                Accordion 3
                            </b-button>
                        </b-card-header>
                        <b-collapse id="accordion-2-6" accordion="my-accordion" role="tabpanel">
                            <b-card-body>
                            <b-card-text>{{ text }}</b-card-text>
                            </b-card-body>
                        </b-collapse>
                        </b-card>
                    </div>
                </b-card>
            </b-col>
        </b-row>-->
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
            <!--
            <div class="col-md-12 mb-3">
                <div class="card text-left">
                    
                    <div class="card-body">
                        <div style="display: flex; justify-content:space-between; align-items:center;" class=" rounded text-center">
                            <form action="action">
                                <div class="">
                                    <div class="form-row">
                                        <div class="form-group">
                                            <div class="input-group">
                                                <input class="form-control" type="text" placeholder="Recipient's username" aria-label="Recipient's username" aria-describedby="basic-addon2" />
                                                <div class="input-group-append"><span class="input-group-text" id="basic-addon2">@example.com</span></div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </form>

                            <b-tabs  
                            active-nav-item-class="nav nav-tabs"
                            content-class="mt-3"
                            >
                            
                            
                        </div>
                        
                        
                        
                    </div>
                </div>
            </div>-->
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
    title: "Accordion"
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
