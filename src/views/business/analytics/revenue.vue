<template>
    <div class="main-content">
      <breadcumb :page="'Revenue Transactions'" :folder="'Revenue'"  :folder2="'Orders'" />
  
      <!-- imageCropper -->
      <!--
      <b-row>
        <b-col md="6 mb-30">
          <b-card title="Input Crop Image">
            <input
              type="file"
              name="image"
              accept="image/*"
              style="font-size: 1.2em; padding: 10px 0;"
              @change="setImage"
            />
  
            <br />
            <div
              style="width: 100%; height:100%; border: 1px solid gray; display: inline-block;"
            >
              <h4>Insert Image</h4>
              <vue-cropper
                ref="cropper"
                :guides="true"
                :view-mode="2"
                drag-mode="crop"
                :auto-crop-area="0.5"
                :min-container-width="250"
                :min-container-height="180"
                :background="true"
                :rotatable="true"
                :src="imgSrc"
                alt="Source Image"
                :img-style="{ width: '400px', height: '300px' }"
              >
              </vue-cropper>
            </div>
  
            <br />
            <br />
  
            <div class="mt-4">
              <b-button
                class="m-2"
                variant="primary"
                @click="cropImage"
                v-if="imgSrc != ''"
                >Crop</b-button
              >
              <b-button
                class="m-2"
                variant="success"
                @click="rotate"
                v-if="imgSrc != ''"
                >Rotate</b-button
              >
            </div>
          </b-card>
        </b-col>
        <b-col md="6">
          <b-card title="Output Crop Image">
            <img
              :src="cropImg"
              style="width: 100%; height: 100%; border: 1px solid gray"
              alt="Cropped Image"
            />
          </b-card>
        </b-col>
      </b-row>-->
  
      <div class="row">
        <b-col md="12">
            <!-- start::basic-tab -->
            <b-card  
            class="card   mb-30" 
            header="Basic Tabs" 
            header-bg-variant="transparent ">
                
                <b-tabs  
                active-nav-item-class="nav nav-tabs"
                content-class="mt-3"
                >
                    <b-tab title="All Transactions" active>
                        <div class="row">
                            <div class="col-md-12 mb-3">
                                <div class="card text-left">
                                    <div class="card-body">
                                        <h4 class="card-title mb-3">All Transaction </h4>
                                        
                                        <div class="table-responsive">
                                            <table class="table">
                                                <thead>
                                                    <tr>
                                                        <th scope="col">Reference</th>
                                                        <th scope="col">Customer</th>
                                                        <th scope="col">Orderid</th>
                                                        <th scope="col">Amount</th>
                                                        <th scope="col">Date</th>
                                                        <th scope="col">Status</th>
                                                        <th scope="col">Payment Type</th>
                                                        <th scope="col">Action</th>
                                                    </tr>
                                                </thead>
                                                <tbody>
                                                    <tr>
                                                        <th scope="row">TR213458WEN</th>
                                                        <td>Smith Doe</td>
                                                        <th scope="row">ASDR34R</th>
                                                        <td>5000</td>
                                                        <td>12-10-2019</td>
                                                        <td><span class="badge badge-warning">Pending</span></td>
                                                        <td>Card</td>
                                                        <td><a class="text-success mr-2" href="#"><i class="nav-icon i-Pen-2 font-weight-bold"></i></a><a class="text-danger mr-2" href="#"><i class="nav-icon i-Close-Window font-weight-bold"></i></a></td>
                                                    </tr>
                                                    <tr>
                                                      <th scope="row">TR213458WEN</th>
                                                      <td>Smith Doe</td>
                                                      <th scope="row">ASDR34R</th>
                                                      <td>5000</td>
                                                      <td>12-10-2019</td>
                                                      <td><span class="badge badge-danger">Canceled</span></td>
                                                      <td>Card</td>
                                                      <td><a class="text-success mr-2" href="#"><i class="nav-icon i-Pen-2 font-weight-bold"></i></a><a class="text-danger mr-2" href="#"><i class="nav-icon i-Close-Window font-weight-bold"></i></a></td>
                                                    </tr>
                                                    <tr>
                                                      <th scope="row">TR213458WEN</th>
                                                      <td>Smith Doe</td>
                                                      <th scope="row">ASDR34R</th>
                                                      <td>5000</td>
                                                      <td>12-10-2019</td>
                                                      <td><span class="badge badge-success">Approved</span></td>
                                                      <td>Card</td>
                                                      <td><a class="text-success mr-2" href="#"><i class="nav-icon i-Pen-2 font-weight-bold"></i></a><a class="text-danger mr-2" href="#"><i class="nav-icon i-Close-Window font-weight-bold"></i></a></td>
                                                    </tr>
                                                </tbody>
                                            </table>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </b-tab>
                    <b-tab title="Approved">
                        <p class="">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.</p>
                    </b-tab>
                    <b-tab title="Canceled" >
                        <p class="">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.</p>
                    </b-tab>
                    <b-tab title="Pending">
                        <p class="">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.</p>
                    </b-tab>
                    
                </b-tabs>         
            </b-card> 
        </b-col>
    </div>
    </div>
  </template>
  <script>
  //import VueCropper from "vue-cropperjs";
  import "cropperjs/dist/cropper.css";
  
  export default {
    components: {
      //VueCropper
    },
    metaInfo: {
      // if no subcomponents specify a metaInfo.title, this title will be used
      title: "Image Cropper"
    },
  
    data() {
      return {
        imgSrc: "",
        cropImg: ""
      };
    },
    methods: {
      setImage(e) {
        const file = e.target.files[0];
        if (!file.type.includes("image/")) {
          alert("Please select an image file");
          return;
        }
        if (typeof FileReader === "function") {
          const reader = new FileReader();
          reader.onload = event => {
            this.imgSrc = event.target.result;
            // rebuild cropperjs with the updated source
            this.$refs.cropper.replace(event.target.result);
          };
          reader.readAsDataURL(file);
        } else {
          alert("Sorry, FileReader API not supported");
        }
      },
      cropImage() {
        // get image data for post processing, e.g. upload or setting image src
        this.cropImg = this.$refs.cropper.getCroppedCanvas().toDataURL();
      },
      rotate() {
        // guess what this does :)
        this.$refs.cropper.rotate(90);
      }
    }
  };
  </script>
  
  