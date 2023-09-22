<template>
    <div class="main-content">
      <breadcumb :page="'Revenue Transactions'" :folder="'Revenue'"  :folder2="'Orders'" />
  
     
  
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
                        <allTranscation/>
                    </b-tab>
                    <b-tab title="Approved">
                        <Approved/>
                    </b-tab>
                    <b-tab title="Canceled" >
                        <Canceled/>
                    </b-tab>
                    <b-tab title="Pending">
                        <Pending/>
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
  import allTranscation from './revenueTable/allTran.vue';
  import Approved from './revenueTable/approved.vue';
  import Pending from './revenueTable/pending.vue';
  import Canceled from './revenueTable/canceled.vue';
  
  export default {
    components: {
      //VueCropper
      allTranscation,
      Approved,
      Pending,
      Canceled,
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
  
  