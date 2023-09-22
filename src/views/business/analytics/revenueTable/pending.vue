<template>
    <div>

    
        <div class="row">
            <div class="col-md-12 mb-3">
                <div class="card text-left">
                    <div class="card-body">
                        <div style="display: flex; justify-content:space-between; align-items:center;">
                            <h4 class="card-title mb-3">All Orders </h4>
                            <b-button size="lg" variant="" @click="addtable()" style="backgroud-color:white;">ADD</b-button>
                        </div>
                        <div class="table-responsive">
                            <table class="table">
                                <thead style="text-align:center;">
                                    <tr>
                                      <th scope="col">#</th>
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
                                <tbody style="text-align:center;">
                                    <tr v-for="(day, index) in openingHours" :key="day.id">
                                    <th scope="row">{{ index + 1 }}</th>
                                    <td>{{ day.reference }} </td>
                                    <td>{{ day.customer }}</td>
                                    <td><strong>{{ day.orderid}}</strong> </td>
                                    <td>{{ day.amount }}</td>
                                    <td>{{ day.date }} </td>
                                    
                                    <td>
                                        <span :class="day.status === 'Pending' ? 'badge badge-info' : 'badge badge-danger' ">
                                        {{ day.status }}
                                        </span>
                                    </td>
                                    <td>{{ day.payment }}</td>
                                    <td>
                                        <b-dropdown text="Actions">
                                        <b-dropdown-item @click="deleteRow(index)">Delete</b-dropdown-item>
                                        <b-dropdown-item @click="editRow(index)">Edit</b-dropdown-item>
                                        
            
                                        </b-dropdown>
                                    </td>
                                
                                    </tr>
                                </tbody>
                            </table>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <b-modal v-model="showEditModal" title="Edit Row">
            <form @submit.prevent="updateTableRow">
              <div class="form-group">
                <label for="editReference">Reference</label>
                <select v-model="editRowData.reference" class="form-control" id="editReference">
                  <option value="TR213458WEN">TR213458WEN</option>
                  <option value="TR213458WEN">TR213458WEN</option>
                  <option value="TR213458WEN">TR213458WEN</option>
                  <option value="TR213458WEN">TR213458WEN</option>
                  <option value="TR213458WEN">TR213458WEN</option>
                  <option value="TR213458WEN">TR213458WEN</option>
                  
                  <!-- ... options for other days ... -->
              </select>
              </div>
              <div class="form-group">
                <label for="editCustomer">Customer</label>
                <input v-model="editRowData.customer" type="text" class="form-control" id="editCustomer">
              </div>
            <div class="form-group">
                <label for="editOrderId">OrderId</label>
                <select v-model="editRowData.orderid" class="form-control" id="editOrderId">
                    <option value="ASDR34R">ASDR34R</option>
                    <option value="ASDR35R">ASDR35R</option>
                    <option value="ASDR36R">ASDR36R</option>
                    <option value="ASDR37R">ASDR34R</option>
                    <option value="ASDR38R">ASDR38R</option>
                    <option value="ASDR39R">ASDR39R</option>
                    
                    <!-- ... options for other days ... -->
                </select>
            </div>
            <div class="form-group">
                <label for="editAmount">Amount</label>
                <input v-model="editRowData.amount" type="text" class="form-control" id="editAmount">
            </div>
            
            <div class="form-group">
                <label for="editDate">Date</label>
                <input v-model="editRowData.date" type="text" class="form-control" id="editDate">
            </div>

          
            
            <div class="form-group">
                <label for="editStatus">Status</label>
                <select v-model="editRowData.status" class="form-control" id="editStatus">
                    <option value="Pending">Pending</option>
                    
                </select>
            </div>

            <div class="form-group">
              <label for="payment">Payment</label>
              
              <select v-model="editRowData.payment" class="form-control" id="payment">
                  <option value="Card">Card</option>
                  <option value="Bank Transfer">Bank Transfer</option>
                  <option value="Cash On Delivery">Cash On Delivery</option>
                  
                  
                  <!-- ... options for other days ... -->
              </select>
          </div>

            <b-button type="submit" variant="primary">Save Changes</b-button>
            <b-button variant="secondary" @click="showEditModal = false">Cancel</b-button>
            </form>
        </b-modal>
        <!-- Add Table Row Modal -->
        <b-modal v-model="showAddModal" title="Add New Row">
           
            <form @submit.prevent="addTableRow">
                <div class="form-group">
                  <label for="Reference">Reference</label>
                  <select v-model="newRow.reference" class="form-control" id="Reference">
                    <option value="TR213458WEN">TR213458WEN</option>
                    <option value="TR213458WEN">TR213458WEN</option>
                    <option value="TR213458WEN">TR213458WEN</option>
                    <option value="TR213458WEN">TR213458WEN</option>
                    <option value="TR213458WEN">TR213458WEN</option>
                    <option value="TR213458WEN">TR213458WEN</option>
                    
                    <!-- ... options for other days ... -->
                </select>
                </div>
                <div class="form-group">
                  <label for="Customer">Customer</label>
                  <input v-model="newRow.customer" type="text" class="form-control" id="Customer">
                </div>
              <div class="form-group">
                  <label for="OrderId">OrderId</label>
                  <select v-model="newRow.orderid" class="form-control" id="OrderId">
                      <option value="ASDR34R">ASDR34R</option>
                      <option value="ASDR35R">ASDR35R</option>
                      <option value="ASDR36R">ASDR36R</option>
                      <option value="ASDR37R">ASDR34R</option>
                      <option value="ASDR38R">ASDR38R</option>
                      <option value="ASDR39R">ASDR39R</option>
                      
                      <!-- ... options for other days ... -->
                  </select>
              </div>
              <div class="form-group">
                  <label for="Amount">Amount</label>
                  <input v-model="newRow.amount" type="text" class="form-control" id="Amount">
              </div>
              
              <div class="form-group">
                  <label for="Date">Date</label>
                  <input v-model="newRow.date" type="text" class="form-control" id="Date">
              </div>

            
              
              <div class="form-group">
                  <label for="Status">Status</label>
                  <select v-model="newRow.status" class="form-control" id="Status">
                    <option value="Pending">Pending</option>
                    
                  </select>
              </div>

              <div class="form-group">
                <label for="payment">Payment</label>
                
                <select v-model="newRow.payment" class="form-control" id="payment">
                    <option value="Card">Card</option>
                    <option value="Bank Transfer">Bank Transfer</option>
                    <option value="Cash On Delivery">Cash On Delivery</option>
                    
                    
                    <!-- ... options for other days ... -->
                </select>
              </div>

              <b-button type="submit" variant="primary">Add</b-button>
              <b-button variant="secondary" @click="showAddModal = false">Cancel</b-button>
            </form>
        </b-modal>
    </div>
</template>


<script>
import { BModal, BButton } from "bootstrap-vue";

export default {
    name: 'Pending',
    metaInfo: {
      // if no subcomponents specify a metaInfo.title, this title will be used
        title: "DropDown"
    },

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
        reference: "",
        customer: "",
        orderid: "",
        amount: "",
        order: "",
        date: "",
        status: "Pending",
        payment: "",
      },
      
      openingHours: [
        {
          id: 1,
          reference: "TR213458WEN",
          customer: "John Smith",
          orderid: "ASDR34R",
          amount: "8000",
          date: "23-05-2014",
          status: "Pending",
          payment: "Card"
        }
       
        
    
        // Add similar data for other days
      ]
    };
  },
  methods: {

    onClick() {
        // Close the menu and (by passing true) return focus to the toggle button
        this.$refs.dropdown.hide(true)
    },

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
        reference: "",
        customer: "",
        orderid: "",
        amount: "",
        order: "",
        date: "",
        status: "Pending",
        payment: "",
      };
      this.showAddModal = false;
    }
    
    
  },
};
</script>