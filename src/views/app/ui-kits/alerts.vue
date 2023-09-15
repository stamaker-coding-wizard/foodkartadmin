<template>
  <div class="main-content">
    <breadcumb :page="'Business Categories'" :folder="'Business'" :folder2="'Plans'" />
    <!--
    <b-row>
      <b-col md="12">
        <b-alert
          show
          variant="alert alert-card alert-warning text-center"
          dismissible=""
        >
          Gull makes development life easier!
          <b-button pill variant="warning ml-3">Buy Now</b-button>
        </b-alert>
        <b-alert show variant="alert alert-card alert-success" dismissible>
          <strong class="text-capitalize">Success!</strong> Lorem ipsum dolor
          sit amet.
        </b-alert>
        <b-alert show variant="alert alert-card alert-danger" dismissible>
          <strong class="text-capitalize">Danger!</strong> Lorem ipsum dolor sit
          amet.
        </b-alert>
        <b-alert show variant="alert alert-card alert-info" dismissible>
          <strong class="text-capitalize">Info!</strong> Lorem ipsum dolor sit
          amet.
        </b-alert>
      </b-col>

      <b-col md="12">
        <b-card title="Bootstrap Alerts" class=" mb-30">
          <b-alert show variant="primary" dismissible>
            <strong class="text-capitalize">Primary!</strong>
            Lorem ipsum dolor sit amet.
          </b-alert>

          <b-alert show variant="success" dismissible>
            <strong class="text-capitalize">Success!</strong>
            Lorem ipsum dolor sit amet.
          </b-alert>

          <b-alert show variant="info" dismissible>
            <strong class="text-capitalize">Info!</strong>
            Lorem ipsum dolor sit amet.
          </b-alert>

          <b-alert show variant="warning" dismissible>
            <strong class="text-capitalize">Warning!</strong>
            Lorem ipsum dolor sit amet.
          </b-alert>

          <b-alert show variant="danger" dismissible>
            <strong class="text-capitalize">Danger!</strong>
            Lorem ipsum dolor sit amet.
          </b-alert>
        </b-card>

        <b-card class="mt-4">
          <b-alert
            :show="dismissCountDown"
            dismissible
            variant="success"
            @dismissed="dismissCountDown = 0"
            @dismiss-count-down="countDownChanged"
          >
            <p>
              This alert will dismiss after {{ dismissCountDown }} seconds...
            </p>
            <b-progress
              variant="success"
              :max="dismissSecs"
              :value="dismissCountDown"
              height="4px"
            ></b-progress>
          </b-alert>

          <b-button @click="showAlert" variant="primary" class="m-1">
            Show alert with count-down timer
          </b-button>
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
        <div class="card text-left">
            <div style="display: flex; justify-content:space-between; background-color:#f1eaea;" class="p-3 rounded text-center">
              <h4 class="card-title mb-3">Store/Restaurant Categories </h4>
              <p>
                <i class="i-Gear"></i>
              </p>
            </div>
            <div class="card-body">
                <div class="table-responsive">
                    <table class="table">
                        <thead style="text-align:center;">
                            <tr>
                                <th scope="col">#</th>
                                <th scope="col">Category Name</th>
                                <th scope="col">Category Type</th>
                                <!--
                                <th scope="col">Price</th>
                                <th scope="col">Status</th>
                                -->
                                <th scope="col">Action</th>
                            </tr>
                        </thead>
                        <tbody style="text-align:center;">
                            <tr>
                                <th scope="row">1</th>
                                <td>Local Food</td>
                                <!--
                                <td>12-10-2019</td>
                                <td>$30</td>-->
                                <td>Food</td>
                                <td><a class="text-success mr-2" href="#"><i class="nav-icon i-Pen-2 font-weight-bold"></i></a><a class="text-danger mr-2" href="#"><i class="nav-icon i-Close-Window font-weight-bold"></i></a></td>
                            </tr>
                            <tr>
                                <th scope="row">2</th>
                                <td>Antibiotics</td>
                                <!--<td>23-10-2019</td>
                                <td>$300</td>-->
                                <td>Drugs</td>
                                <td><a class="text-success mr-2" href="#"><i class="nav-icon i-Pen-2 font-weight-bold"></i></a><a class="text-danger mr-2" href="#"><i class="nav-icon i-Close-Window font-weight-bold"></i></a></td>
                            </tr>
                            <tr>
                                <th scope="row">3</th>
                                <td>Antibiotics</td>
                                <!--
                                <td>12-10-2019</td>
                                <td>$30</td>-->
                                <td>Drugs</td>
                                <td><a class="text-success mr-2" href="#"><i class="nav-icon i-Pen-2 font-weight-bold"></i></a><a class="text-danger mr-2" href="#"><i class="nav-icon i-Close-Window font-weight-bold"></i></a></td>
                            </tr>
                            <tr>
                              <th scope="row">4</th>
                              <td>Antibiotics</td>
                              <!--
                              <td>12-10-2019</td>
                              <td>$30</td>-->
                              <td>Drugs</td>
                              <td><a class="text-success mr-2" href="#"><i class="nav-icon i-Pen-2 font-weight-bold"></i></a><a class="text-danger mr-2" href="#"><i class="nav-icon i-Close-Window font-weight-bold"></i></a></td>
                          </tr>
                          <tr>
                            <th scope="row">5</th>
                            <td>Antibiotics</td>
                            <!--
                            <td>12-10-2019</td>
                            <td>$30</td>-->
                            <td>Drugs</td>
                            <td><a class="text-success mr-2" href="#"><i class="nav-icon i-Pen-2 font-weight-bold"></i></a><a class="text-danger mr-2" href="#"><i class="nav-icon i-Close-Window font-weight-bold"></i></a></td>
                        </tr>
                        </tbody>
                    </table>
                </div>
            </div>
        </div>
    </div>
    </div>
  </div>
</template>
<script>
export default {
  metaInfo: {
    // if no subcomponents specify a metaInfo.title, this title will be used
    title: "Alerts"
  },
  data() {
    return {
      dismissSecs: 10,
      dismissCountDown: 0,
      showDismissibleAlert: false
    };
  },
  methods: {
    countDownChanged(dismissCountDown) {
      this.dismissCountDown = dismissCountDown;
    },
    showAlert() {
      this.dismissCountDown = this.dismissSecs;
    }
  }
};
</script>
