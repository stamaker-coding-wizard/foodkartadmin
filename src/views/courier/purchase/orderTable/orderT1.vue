<template>
   <div>
        <div style="display: flex; justify-content:space-between; background-color:#fff;" class="p-3 rounded text-center">
            <h4 class="card-title mb-3">Exclusive datatable plugin</h4>
            <p>
            <!--<button @click="addTableRow()" style="background-color:#fff; p-3">ADD</button>-->
            </p>
        </div>
        <div class="table-responsive">
            <!-- Table 1 -->
            <table class="table">
                <thead>
                    <tr>
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
                    <tr v-for="(person, index) in people" :key="index">
                        <td>
                            <input type="checkbox" v-model="person.selected">
                        </td>
                        <td><img :src="person.recipent" class="img"></td>
                        <td><img :src="person.Merchant" class="img"></td>
                        <td> {{person.status}} </td>
                        <td>
                            <b-button :variant="getColorVariant(index)" class="m-1">{{ person.items }}</b-button>
                        </td>
                        
                    
                        <td>{{person.fees1}}
                            <br> {{ person.fees2 }}
                        </td>
                        <td>
                            <b-dropdown id="dropdown-1" text="Dropdown">
                            <b-dropdown-item @click="deleteSelected(person)">Delete</b-dropdown-item>
                            <b-dropdown-item @click="editItemClick(person)">Edit</b-dropdown-item>
                                
                            </b-dropdown>
                        </td>

                        <!-- Add more columns as needed -->
                    </tr>
                </tbody>
            </table>

            

            <!-- Add Row Modal -->
            <b-modal v-model="addRowModal" title="Add Row">
                <!-- Form for adding a new row -->
                <form @submit.prevent="addTableRow">
                    <!-- Add input fields for the new row here -->
                    <!-- Example: -->
                    <div class="form-group">
                        <label for="newRecipient">Recipient:</label>
                        <input type="text" class="form-control" v-model="newRow.recipent">
                    </div>
                    <div class="form-group">
                        <label for="newStatus">Status:</label>
                        <input type="text" class="form-control" v-model="newRow.status">
                    </div>
                    
                    <!-- Add more fields as needed -->
                    <button type="submit" class="btn btn-primary">Add</button>
                </form>
            </b-modal>

            <!-- Edit Row Modal -->
            <b-modal v-model="editRowModal" title="Edit Row">
                <!-- Form for editing the selected row -->
                <form @submit.prevent="saveEditedRow">
                <!-- Populate input fields with data from selectedRow -->
                <!-- Example: -->
                <div class="form-group">
                    <label for="editRecipient">Recipient:</label>
                    <input type="text" class="form-control" v-model="selectedRow.recipent">
                </div>
                <div class="form-group">
                    <label for="editStatus">Status:</label>
                    <input type="text" class="form-control" v-model="selectedRow.status">
                </div>
                <!-- Add more fields as needed -->
                <button type="submit" class="btn btn-primary">Save</button>
                </form>
            </b-modal>
        </div>
   </div>
</template>

<script>
export default{
    name: 'orderT1',
    data(){
        return{
            // New data properties for modals and editing
            addRowModal: false,
            editRowModal: false,
            selectedRow: {},
            newRow: {
                // Initialize with default values for the new row fields
                recipent: '',
                status: '',
                // Add more fields as needed
            },

            colorVariants: ['warning', 'primary', 'success', 'info', 'danger'], // Define your color variants
            first_table: true,
            second_table: false,
            perPage: 5,
            currentPage: 1,
            
            people: [
                { selected: false, recipent: require("@/assets/images/products/foodkart-image.jpg"), Merchant: require("@/assets/images/products/foodkart-image.jpg"), status: '11/28/2016', items: 'Waiting',  fees1:'UI Lib', fees2:'Angular 2.Vue.js'},
                { selected: false, recipent: require("@/assets/images/products/foodkart-image.jpg"), Merchant: require("@/assets/images/products/foodkart-image.jpg"), status: '11/28/2016', items: 'Waiting',  fees1:'UI Lib', fees2:'Angular 2.Vue.js' },
                { selected: false, recipent: require("@/assets/images/products/foodkart-image.jpg"), Merchant: require("@/assets/images/products/foodkart-image.jpg"), status: '11/28/2016', items: 'Delivered', fees1:'UI Lib', fees2:'Angular 2.Vue.js' },
                { selected: false, recipent: require("@/assets/images/products/foodkart-image.jpg"), Merchant: require("@/assets/images/products/foodkart-image.jpg"), status: '11/28/2016', items: 'Delivered', fees1:'UI Lib', fees2:'Angular 2.Vue.js'},
                { selected: false, recipent: require("@/assets/images/products/foodkart-image.jpg"), Merchant: require("@/assets/images/products/foodkart-image.jpg"), status: '11/28/2016', items: 'Processing',  fees1:'UI Lib', fees2:'Angular 2.Vue.js' }
                
            ],
            people2: [
                { selected: false, recipent: require("@/assets/images/products/foodkart-image.jpg"), Merchant: '11/28/2017', status: 'Processing',  items1:'UI Lib', items2:'Angular 2.Vue.js'},
                { selected: false, recipent: require("@/assets/images/products/foodkart-image2.jpg"), Merchant: '11/28/2017', status: 'Processing',  items1:'UI Lib', items2:'Angular 2.Vue.js'  },
                { selected: false, recipent: require("@/assets/images/products/foodkart-image3.jpg"), Merchant: '11/28/2017', status: 'Processing',   items1:'UI Lib', items2:'Angular 2.Vue.js' },
                { selected: false, recipent: require("@/assets/images/products/foodkart-image.jpg"), Merchant: '11/28/2017', status: 'Processing',  items1:'UI Lib', items2:'Angular 2.Vue.js'},
                { selected: false, recipent: require("@/assets/images/products/foodkart-image2.jpg"), Merchant: '11/28/2017', status: 'Processing', items1:'UI Lib', items2:'Angular 2.Vue.js' }
                
            ]
           
        }
    },
    computed: {
      rows() {
        return this.items.length
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
            status: '',
            // Initialize other fields as needed
        };
        },


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
