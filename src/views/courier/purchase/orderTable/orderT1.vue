<template>
   <div>
        <div style="display: flex; justify-content:space-between;align-items:center; background-color:#fff;" class="p-3 rounded text-center">
            <h4 class="card-title mb-3">Exclusive datatable plugin</h4>
            <p>
                <b-button variant="primary ripple btn-icon m-1" @click="addTableRow()" style="border-radius:25px;">
                
                    <span class="ul-btn__text ml-1">ADD</span>
                </b-button>
            </p>
        </div>
        <div class="table-responsive">
            <!-- Table 1 -->
            <table class="table">
                <thead>
                    <tr style="text-align:center;">
                        <th scope="col">#</th>
                        <th scope="col">Recipent </th>
                        <th scope="col">Merchant</th>
                        <th scope="col">Status</th>
                        <th scope="col">Item</th>
                        <th scope="col">Fees</th>
                        <th scope="col">Actions</th>
                        <!-- Add more headers as needed -->
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="(person, index) in people" :key="index" style="text-align:center;">
                        <td>
                            <input type="checkbox" v-model="person.selected">
                        </td>
                        <td><img v-bind:src="person.recipent" class="img"></td>
                        <td><h5>{{ person.Merchant }}</h5></td>
                        
                        <td>
                            <b-button :variant="getColorVariant(index)" class="m-1">{{ person.status }}</b-button>
                        </td>
                        <td> {{person.items}} </td>
                        
                    
                        <td>{{person.fees}}
                            
                        </td>
                        <td>
                          
                            <!--<a class="text-success mr-2" @click="editItemClick(person)" style="cursor:pointer;"><i class="nav-icon i-Pen-2 font-weight-bold"></i></a>-->

                            <a class="text-danger mr-2" @click="addChatRow(index)" style="cursor:pointer;"><i class="nav-icon i-Speach-Bubble-3 font-weight-bold"></i></a>

                            <!--<a class="text-danger mr-2" @click="deleteSelected(person)" style="cursor:pointer;"><i class="nav-icon i-Close-Window font-weight-bold"></i></a>-->
                            
                        </td>
                        <!-- Add more columns as needed -->
                    </tr>
                </tbody>
            </table>

            

            <!-- Add Row Modal -->
            <b-modal v-model="addRowModal" title="Add Row">
                <!-- Form for adding a new row -->
                <form @submit.prevent="addTableRow">
                    
                    <!--
                    <div class="form-group">
                        <label for="newRecipient">Recipient:</label>
                        <input type="text" class="form-control" v-model="newRow.recipent">
                    </div>
                    <div class="form-group">
                        <label for="newStatus">Status:</label>
                        <input type="text" class="form-control" v-model="newRow.status">
                    </div>
                    <div class="form-group">
                        <label for="newItems">Items:</label>
                        
                        <select v-model="newRow.items" class="form-control" id="newItems">
                            <option value="Pending">Pending</option>
                            <option value="Waiting">Waiting</option>
                            <option value="Delivered">Delivered</option>
                            <option value="Processing">Processing</option>
                            
                      
                           
                        </select>
                    </div>
                    
                   
                    <button type="submit" class="btn btn-primary">Add</button>
                -->
                </form>
            </b-modal>

            <!-- Edit Row Modal -->
            <b-modal v-model="editRowModal" title="Edit Row">
                <!-- Form for editing the selected row -->
                <form @submit.prevent="saveEditedRow">
                <!--
                <div class="form-group">
                    <label for="editStatus">Status:</label>
                    <input type="text" class="form-control" v-model="selectedRow.status">
                    
                </div>
                <div class="form-group">
                    <label for="editItems">Items:</label>
            
                    <select v-model="selectedRow.items" class="form-control" id="editItems">
                        <option value="Pending">Pending</option>
                        <option value="Waiting">Waiting</option>
                        <option value="Delivered">Delivered</option>
                        <option value="Processing">Processing</option>
                        
                       
                    </select>
                </div>
                 <div class="form-group">
                    <label for="editFees1">Fees1:</label>
                    <input type="text" class="form-control" v-model="selectedRow.fees1">
                </div>
                <div class="form-group">
                    <label for="editFees2">Fees2:</label>
                    <input type="text" class="form-control" v-model="selectedRow.fees2">
                </div>
                
                <button type="submit" class="btn btn-primary">Save</button>
            -->
                </form>
            </b-modal>
            <!--Adding Chart Modal -->
            <b-modal v-model="showJohnChat" size="lg">
                <JohnChat/>
            </b-modal>
        </div>
   </div>
</template>

<script>
import JohnChat from "../OrderChat/John.vue";
export default{
    name: 'orderT1',
    components: {
        JohnChat,
    },
    data(){
        return{
            
            // New data properties for modals and editing
            addRowModal: false,
            editRowModal: false,
            selectedRow: {},
            showJohnChat: false, //Control chart modal visibility
            newRow: {
                // Initialize with default values for the new row fields
                recipent: '',
                imgUrl: '',
                status: '',
                items: '',
                fees: '',
                
                // Add more fields as needed
            },

            colorVariants: ['warning', 'primary', 'success', 'info', 'danger'], // Define your color variants
            first_table: true,
            second_table: false,
            perPage: 5,
            currentPage: 1,
            
            people: [
                { selected: false, name: 'potato', recipent: require("@/assets/images/products/foodkart-image.jpg"), Merchant: "John Smoker", items: 'Food', status: 'Waiting',  fees:'5000'},
                { selected: false, name: 'yam', recipent: require("@/assets/images/products/foodkart-image2.jpg"), Merchant: "Taofeek Smoker", items: 'Food', status: 'Waiting',  fees:'5000' },
                { selected: false, name: 'egg', recipent: require("@/assets/images/products/foodkart-image3.jpg"), Merchant: "Caro Smoker", items: 'Food', status: 'Delivered', fees:'5000' },
                { selected: false, name: 'potatoss', recipent: require("@/assets/images/products/foodkart-image4.jpg"), Merchant: "Sarah Smoker", items: 'Food', status: 'Delivered', fees:'5000'},
                { selected: false, name: 'orange', recipent: require("@/assets/images/products/foodkart-image2.jpg"), Merchant: "Doe Smoker", items: 'Food', status: 'Processing',  fees:'5000' }
                
            ]
            
           
        }
    },
    computed: {
      rows() {
        return this.status.length
      }
    },
    methods: {
        deleteSelected() {
          // Create a new array without the selected people
          this.people = this.people.filter(person => !person.selected);
          this.people2 = this.people2.filter(person => !person.selected);
        },
        // Function to determine the button variant based on the table index
        getColorVariant(index) {
        // Assign a color variant based on the index of the person
            const variantIndex = index % this.colorVariants.length;
            return `outline-${this.colorVariants[variantIndex]}`;
        },

        nextPage(){
            this.second_table = true
            this.first_table = false
        },
        prevPage(){
            this.second_table = false
            this.first_table = true
        },

        // Open the edit modal and set the selected row
        editItemClick(person) {
        this.selectedRow = { ...person };
        this.editRowModal = true;
        },

        // Save the edited row and close the modal
        saveEditedRow() {
        // Implement your logic to save the edited row here
        // You can update the 'people' array with the edited data
        // For example:
        const index = this.people.findIndex(person => person.selected);
        if (index !== -1) {
            this.people[index] = { ...this.selectedRow };
        }
        this.editRowModal = false;
        },

        // Open the add modal
        addTableRow() {
        this.addRowModal = true;
        },

         // Add a new row to the table
        addNewRow() {
        // Implement your logic to add a new row here
        // You can push the 'newRow' data to the 'people' array
        // For example:
        this.people.push({ ...this.newRow, selected: false });
        this.addRowModal = false;
        // Clear the newRow data for the next entry
        this.newRow = {
            recipent: '',
            imgUrl: '',
            status: '',
            items: '',
            fees1: '',
            fees2: '',
            // Initialize other fields as needed
        };
        },
        addChatRow(){
      
            this.showJohnChat = true;
        }


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
