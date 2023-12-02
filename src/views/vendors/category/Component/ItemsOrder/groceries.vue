<template>
    <div>
        <h3>Popular Groceries</h3>
        <b-row>
            <!-- ICON BG -->
            <b-col lg="3" md="6" sm="12" v-for="grocery in groceries" :key="grocery.Content" style="cursor:pointer;" class="categoryBox">
                
              <b-card
                class=" o-hidden mb-30 categoryCard"
              >
                <p class="status">{{ grocery.status }} </p>
                <div class="cateUrl">
                    <img :src="grocery.Url">
                </div>
                <div class="cateContent">
                    <div class="namePrice">
                        <h6 class="name">{{ grocery.name }} </h6>
                        <h4 class="price">{{ grocery.price}}</h4>
                    </div>
                    <!--
                  <div class="actions">
                    <a class="text-success mr-2" @click="editRow(index)" style="cursor:pointer;"><i class="nav-icon i-Pen-2 font-weight-bold"> <span class="action">Edit</span> </i></a>
                      
                    <a class="text-danger mr-2" @click="deleteRow(index)" style="cursor:pointer;"><i class="nav-icon i-Close-Window font-weight-bold"><span class="action">Delete</span></i></a>
                  </div>-->
                  <div class="actions">
                    <h5><span class="vendor">Vendor:</span> <span class="vendorN"> {{ grocery.vendor }} <a class="text-success mr-2 ml-2" @click="addChatRow(index)" style="cursor:pointer;"><i class="nav-icon i-Speach-Bubble-3 font-weight-bold"></i></a> </span> </h5>
                </div>
                  
                </div>
              </b-card>
            </b-col>
              
        </b-row>
       
        <!-- Edit Table Row Modal -->
      <b-modal v-model="showEditModal" title="Edit Row">
        <form @submit.prevent="updateTableRow">
          <!--
          <div class="form-group">
            <label for="editfoodImg">Food Image</label>
            
          
            <div v-model="editRowData.Url" class="custom-dropdown" id="editfoodImg">
              <div class="selected-option" @click="toggleDropdown">
                <img src="../../../assets/images/products/foodkart1.jpg" alt="Option 1" style="width:60px;height:60px;"> {{ selectedOption }}
              </div>
              <div class="dropdown-options" v-show="isOpen">
                <div @click="selectOption('Option 1')">
                  <img src="../../../assets/images/products/foodkart2.jpg" alt="Option 1" style="width:60px;height:60px;"> Option 1
                </div>
                <div @click="selectOption('Option 2')">
                  <img src="../../../assets/images/products/foodkart3.jpg" alt="Option 2" style="width:60px;height:60px;"> Option 2
                </div>
              </div>
            </div>
            
          </div>
          
          <div class="form-group">
            <label for="editFoodName">Food Name</label>
            
            <select v-model="editRowData.name" class="form-control" id="editFoodName">
              <option value="Beans and Bread">Beans and Bread</option>
              <option value="Jollof Rice">Jollof Rice</option>
              <option value="Semo and Egunsi">Semo and Egunsi</option>
              
            </select>
            
          </div>
          <div class="form-group">
            <label for="editFoodVendor">Food Vendor</label>
            
            <select v-model="editRowData.vendor" class="form-control" id="editFoodVendor">
              <option value="Johnson">Johnson</option>
              <option value="Mary">Mary</option>
              
              
            </select>
          </div>
          <div class="form-group">
            <label for="editPrice">Price</label>
            <input v-model="editRowData.price" type="text" class="form-control" id="editPrice">
          </div>
          <div class="form-group">
            <label for="editFoodStatus">Food Status</label>
            
            <select v-model="editRowData.status" class="form-control" id="editFoodStatus">
              <option value="Sale">Sale</option>
              <option value="Not Available">Not Available</option>
              
            </select>
            
          </div>
        
          
          <b-button type="submit" variant="primary">Save Changes</b-button>
          <b-button variant="secondary" @click="showEditModal = false">Cancel</b-button>-->
        </form>
      </b-modal>

        <!-- Add Table Row Modal -->
      <b-modal v-model="showAddModal" title="Add New Row">
        <form @submit.prevent="addTableRow">
          
          <!--
          <div class="form-group">
            <label for="newImage">Food Image</label>
            
          
            <div v-model="newRow.Url" class="custom-dropdown" id="newImage">
              <div class="selected-option" @click="toggleDropdown">
                <img src="../../../assets/images/products/foodkart1.jpg" alt="Option 1" style="width:60px;height:60px;"> {{ selectedOption }}
              </div>
              <div class="dropdown-options" v-show="isOpen">
                <div @click="selectOption('Option 1')">
                  <img src="../../../assets/images/products/foodkart2.jpg" alt="Option 1" style="width:60px;height:60px;"> Option 1
                </div>
                <div @click="selectOption('Option 2')">
                  <img src="../../../assets/images/products/foodkart3.jpg" alt="Option 2" style="width:60px;height:60px;"> Option 2
                </div>
              </div>
            </div>
            
          </div>
          
          <div class="form-group">
            <label for="newName">Food Name</label>
            
            <select v-model="newRow.name" class="form-control" id="newName">
              <option value="Beans and Bread">Beans and Bread</option>
              <option value="Jollof Rice">Jollof Rice</option>
              <option value="Semo and Egunsi">Semo and Egunsi</option>
              
            </select>
            
          </div>
          <div class="form-group">
            <label for="newVendor">Food Vendor</label>
            
            <select v-model="newRow.vendor" class="form-control" id="newVendor">
              <option value="Johnson">Johnson</option>
              <option value="Mary">Mary</option>
              
              
            </select>
          </div>
          <div class="form-group">
            <label for="newPrice">Price</label>
            <input v-model="newRow.price" type="text" class="form-control" id="newPrice">
          </div>
          <div class="form-group">
            <label for="newStatus">Food Status</label>
            
            <select v-model="newRow.status" class="form-control" id="newStatus">
              <option value="Sale">Sale</option>
              <option value="Not Available">Not Available</option>
              
            </select>
            
          </div>
          <b-button type="submit" variant="primary">Add</b-button>
          <b-button variant="secondary" @click="showAddModal = false">Cancel</b-button>-->
        </form>
      </b-modal>
      <b-modal v-model="showGroceriesChart" size="lg">
        <GroceriesChat/>
      </b-modal>
    </div>
</template>

<script>
import { BModal } from "bootstrap-vue";
import GroceriesChat from "./chat/Products.vue";
export default {
    name: 'groceries',
    components: {
    // Register Bootstrap-Vue components
      BModal,
      GroceriesChat,
      
    },

    data(){
        return{
            showEditModal: false, // Control edit modal visibility
            editRowData: {}, // Data for the row being edited
            editRowIndex: -1, // Index of the row being edited
            showGroceriesChart: false, //Control chart modal visibility

            showAddModal: false, // Control modal visibility

            isOpen: true,
            selectedOption: 'Option 1',


            newRow: {
              status: "",
              Url: "",
              name: "",
              price: "",
              vendor: "",
              
              
            },
            groceries: [
                {Url: require("@/assets/images/products/groceries1-removebg-preview.png"), name:"NetCafe", status:"Sale", price: "1000", vendor: "Sarah"},
                {Url: require("@/assets/images/products/sausage-removebg-preview.png"), name:"Sausage", status:"Not Available",price: "2000", vendor: "Sarah" },
                {Url: require("@/assets/images/products/shawama-removebg-preview.png"), name:"Shawama", status:"Sale", price: "1000", vendor: "Tomi" },
                {Url: require("@/assets/images/products/groceries2-removebg-preview.png"), name:"Fast Food", status:"Sale", price: "900", vendor: "Ewa" },
                {Url: require("@/assets/images/products/groceries1-removebg-preview.png"), name:"NetCafe", status:"Sale", price: "4000", vendor: "Taofeek"},
                {Url: require("@/assets/images/products/sausage-removebg-preview.png"), name:"Sausage", status:"Not Available", price: "5000", vendor: "Ayomide" },
                {Url: require("@/assets/images/products/shawama-removebg-preview.png"), name:"Shawama", status:"Sale", price: "6000", vendor: "Bobo" },
                {Url: require("@/assets/images/products/groceries2-removebg-preview.png"), name:"Fast Food", status:"Sale", price: "7000", vendor: "Bamidele" },

                
            ]
           
        }
    },
    methods: {

editRow(index) {
  // Open the edit modal with data from the selected row
  this.editRowData = { ...this.groceries[index] };
  this.editRowIndex = index;
  this.showEditModal = true;
},
updateTableRow() {
  // Update the row data with the edited values
  if (this.editRowIndex !== -1) {
    this.groceries[this.editRowIndex] = { ...this.editRowData };
  }

  // Reset edit modal data and hide the modal
  this.editRowData = {};
  this.editRowIndex = -1;
  this.showEditModal = false;
},


deleteRow(index) {
  // Remove the row from the openingHours array
  this.groceries.splice(index, 1);
},
addtable() {
  // Show the modal when the "ADD" button is clicked
  this.showAddModal = true;
},
addTableRow() {
  // Add the new row to the openingHours array
  this.groceries.push({ ...this.newRow, id: this.groceries.length + 1 });
  
  // Reset the form and hide the modal
  this.newRow = {
    status: "",
    Url: "",
    name: "",
    price: "",
    vendor: "",
  };
  this.showAddModal = false;
},
toggleDropdown() {
  this.isOpen = !this.isOpen;
},
selectOption(option) {
  this.selectedOption = option;
  this.isOpen = false; // Close the dropdown when an option is selected
},
addChatRow(){
      
      this.showGroceriesChart = true;
  }


},

}
</script>



<style scoped>
.categoryCard{
  position: relative;
  height: fit-content;
  
}
.status{
  position: absolute;
  top: 0;
  left: 0;
  background-color: #10b981 !important;
  width: fit-content;
  padding: 5px 15px;
  text-align: left;
  color:#fff;
  text-align: left;
  font-weight: 500;
  font-family: sans-serif;

  display: none;
}
.categoryBox:hover .status{
  display: block;
}
.categoryBox:hover .categoryCard{
  border: 3px solid #10b981 !important;
}
.cateUrl{
  width: 100%;
  height: 110px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 20px;
  margin-bottom: 25px;
}
.cateUrl img{
  width: 150px;
  height: 100%;

  object-fit: cover;
}
.name{
  color: gray;
  font-size: 18px;
  font-weight: 400;
  
}
.namePrice{
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    margin-bottom: 10px;
}
.price{
  font-size: 20px;
  font-weight: 700;
  color:#000;
}
.actions{
  width: 100%;
  text-align: center;
}
.action{
  color: gray;
  cursor: pointer;
}
.vendor{
    color: #10b981;
    font-size: 16px;
    font-weight: 800;
}
.vendorN{
    color: gray;
    font-weight: 500;
    font-size: 16px;
}

</style>