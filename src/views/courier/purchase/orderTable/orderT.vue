<template>
    <div>
        <div class="card text-left">
            
                  
            <orderT1 v-show="first_table"/>
            
            <!-- Table 2 -->
            <orderT2 v-show="second_table"/>
  
              
          
          <!-- Pagination Controls -->
          <div class="pagination m-5">
              <button @click="prevPage" class="btn btn-secondary">Previous Page</button>
              <button @click="nextPage" class="btn btn-secondary ml-3">Next Page</button>
          </div>

              
        </div>


        
    </div>
</template>


<script>
import orderT1 from './orderT1.vue';
import orderT2 from './orderT2.vue';
export default{
    name: 'orderTable',
    components: {
        orderT1,
        orderT2,
    },
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
        editItem2Click(person2) {
        this.selectedRow = { ...person2 };
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
        saveEditedRow2() {
        // Implement your logic to save the edited row here
        // You can update the 'people' array with the edited data
        // For example:
        const index = this.people2.findIndex(person => person.selected);
        
        if (index !== -1) {
            this.people2[index] = { ...this.selectedRow };
        }
        this.editRowModal = false;
        },
        

        // Open the add modal
        addTableRow() {
        this.addRowModal = true;
        },

        // Open the add modal
        addTableRow2() {
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

         // Add a new row to the table
         addNewRow2() {
        // Implement your logic to add a new row here
        // You can push the 'newRow' data to the 'people' array
        // For example:
        this.people2.push({ ...this.newRow, selected: false });
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
