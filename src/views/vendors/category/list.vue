<template>
    <div class="main-content">
      <breadcumb :page="'Business Hours'" :folder="'Business'" :folder2="'Hours'" />
     
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
          <div style="display: flex; justify-content:space-between; align-items:center; background-color:#fff;" class="p-3 rounded text-center">
            <h4 class="card-title mb-3">Store/Restaurant Categories </h4>
            
            <b-button variant="primary ripple btn-icon m-1" @click="addtable()" style="border-radius:25px">
              
              <span class="ul-btn__text ml-1">ADD</span>
            </b-button>
          </div>
          <div class="card-body">
            <div class="table-responsive">
                <table class="table">
                    <thead style="text-align:center;">
                      <tr>
                        <th scope="col">#</th>
                        <th scope="col">Category Name</th>
                        <th scope="col">Category Type</th>
                        
                        <th scope="col">Action</th>
                      </tr>
                    </thead>
                    <tbody style="text-align:center;">
                      <tr v-for="(day, index) in openingHours" :key="day.id">
                        <th scope="row">{{ index + 1 }}</th>
                        <td>{{ day.categoryName }}</td>
                        <td>{{ day.categoryType }}</td>
                        
                        
                        <td>
                          
                          <a class="text-success mr-2" @click="editRow(index)" style="cursor:pointer;"><i class="nav-icon i-Pen-2 font-weight-bold"></i></a>

                          <a class="text-danger mr-2" @click="deleteRow(index)" style="cursor:pointer;"><i class="nav-icon i-Close-Window font-weight-bold"></i></a>
                        </td>
                  
                      </tr>
                    </tbody>
                  
                </table>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Edit Table Row Modal -->
    <b-modal v-model="showEditModal" title="Edit Row">
      <form @submit.prevent="updateTableRow">
        <!--
        <div class="form-group">
          <label for="editCateName">Category Name</label>
          <select v-model="editRowData.categoryName" class="form-control" id="editCateName">
            <option value="Local Food">Local Food</option>
            <option value="Antibiotics">Antibiotics</option>
            
           
          </select>
        </div>
        <div class="form-group">
          <label for="editCateType">Category Type</label>
          
          <select v-model="editRowData.categoryType" class="form-control" id="editCateType">
            <option value="Food">Food</option>
            <option value="Drugs">Drugs</option>
          
          </select>
        </div>
        
        <b-button type="submit" variant="primary">Save Changes</b-button>
        <b-button variant="secondary" @click="showEditModal = false">Cancel</b-button>
      -->
      </form>
    </b-modal>

    <!-- Add Table Row Modal -->
    <b-modal v-model="showAddModal" title="Add New Row">
      <form @submit.prevent="addTableRow">
        <!--
        <div class="form-group">
          <label for="CateName">Category Name</label>
          <select v-model="newRow.categoryName" class="form-control" id="CateName">
            <option value="Local Food">Local Food</option>
            <option value="Antibiotics">Antibiotics</option>
            
          </select>
        </div>
        <div class="form-group">
          <label for="CateType">Category Type</label>
          

          <select v-model="newRow.categoryType" class="form-control" id="CateType">
            <option value="Food">Food</option>
            <option value="Drugs">Drugs</option>
            
          </select>
        </div>
        
        <b-button type="submit" variant="primary">Add</b-button>
        <b-button variant="secondary" @click="showAddModal = false">Cancel</b-button>
      -->
      </form>
    </b-modal>
  </div>
  </template>
  

<script>
import { BModal, BButton } from "bootstrap-vue";

export default {

  components: {
    // Register Bootstrap-Vue components
    BModal,
    BButton,
  },
  
  
  data() {
    return {

      showEditModal: false, // Control edit modal visibility
      editRowData: {}, // Data for the row being edited
      editRowIndex: -1, // Index of the row being edited

      showAddModal: false, // Control modal visibility
      newRow: {
       
        categoryName: "",
        categoryType: "",
        
      },
      
      openingHours: [
        {
          id: 1,
         
          categoryName: "Local Food",
          categoryType: "Food",
          
        },
        {
          id: 2,
          categoryName: "Antibiotics",
          categoryType: "Drugs",
        },
        {
          id: 3,
          categoryName: "Antibiotics",
          categoryType: "Drugs",
        },
        {
          id: 4,
          categoryName: "Antibiotics",
          categoryType: "Drugs",
        },
        {
          id: 5,
          categoryName: "Antibiotics",
          categoryType: "Drugs",
        },
        
        // Add similar data for other days
      ]
    };
  },
  methods: {

    editRow(index) {
      // Open the edit modal with data from the selected row
      this.editRowData = { ...this.openingHours[index] };
      this.editRowIndex = index;
      this.showEditModal = true;
    },
    updateTableRow() {
      // Update the row data with the edited values
      if (this.editRowIndex !== -1) {
        this.openingHours[this.editRowIndex] = { ...this.editRowData };
      }

      // Reset edit modal data and hide the modal
      this.editRowData = {};
      this.editRowIndex = -1;
      this.showEditModal = false;
    },


    deleteRow(index) {
      // Remove the row from the openingHours array
      this.openingHours.splice(index, 1);
    },
    addtable() {
      // Show the modal when the "ADD" button is clicked
      this.showAddModal = true;
    },
    addTableRow() {
      // Add the new row to the openingHours array
      this.openingHours.push({ ...this.newRow, id: this.openingHours.length + 1 });
      
      // Reset the form and hide the modal
      this.newRow = {
        categoryName: "",
        categoryType: "",
      };
      this.showAddModal = false;
    }
    
    
  },
};
</script>