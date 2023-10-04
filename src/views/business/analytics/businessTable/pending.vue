<template>
    <div>

    
        <div class="row">
            <div class="col-md-12 mb-3">
                <div class="card text-left">
                    <div class="card-body">
                        <div style="display: flex; justify-content:space-between; align-items:center;">
                            <h4 class="card-title mb-3">Pending </h4>
                            <b-button variant="primary ripple btn-icon m-1" @click="addtable()" style="border-radius:25px">
                                
                                <span class="ul-btn__text ml-1">ADD</span>
                            </b-button>
                        </div>
                        <div class="table-responsive">
                            <table class="table">
                                <thead style="text-align:center;">
                                    <tr>
                                        <th scope="col">#</th>
                                        <th scope="col">Orderid</th>
                                        <th scope="col">Customer</th>
                                        <th scope="col">Order</th>
                                        <th scope="col">Delivery Date and <br> Time</th>
                                        <th scope="col">Order <br> Price</th>
                                        <th scope="col">Order <br> Status</th>
                                        <th scope="col">Payment <br> Type</th>
                                        <th scope="col">Action</th>
                                    </tr>
                                </thead>
                                <tbody style="text-align:center;">
                                    <tr v-for="(day, index) in openingHours" :key="day.id">
                                    <th scope="row">{{ index + 1 }}</th>
                                    <td><strong>{{ day.orderid}}</strong> </td>
                                    <td>{{ day.customer }}</td>
                                    <td>{{ day.order }}</td>
                                    <td>{{ day.deliveryDate }}</td>
                                    <td>{{ day.orderPrice }}</td>
                                    
                                    <td>
                                        <span :class="day.status === 'Pending' ? 'badge badge-danger' : 'badge badge-success'">
                                        {{ day.status }}
                                        </span>
                                    </td>
                                    <td>{{ day.payment }}</td>
                                    <td>
                          
                                        <a class="text-success mr-2" @click="editRow(index)" style="cursor:pointer;"><i class="nav-icon i-Pen-2 font-weight-bold"></i></a>
  
                                        <a class="text-danger mr-2" @click="addChatRow(index)" style="cursor:pointer;"><i class="nav-icon i-Speach-Bubble-3 font-weight-bold"></i></a>
  
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

        <b-modal v-model="showEditModal" title="Edit Row">
            <form @submit.prevent="updateTableRow">
                <!--
            <div class="form-group">
                <label for="editOrderId">OrderId</label>
                <select v-model="editRowData.orderid" class="form-control" id="editOrderId">
                    <option value="ASDR34R">ASDR34R</option>
                    <option value="ASDR35R">ASDR35R</option>
                    <option value="ASDR36R">ASDR36R</option>
                    <option value="ASDR37R">ASDR34R</option>
                    <option value="ASDR38R">ASDR38R</option>
                    <option value="ASDR39R">ASDR39R</option>
                    
                    
                </select>
            </div>
            <div class="form-group">
                <label for="editCustomer">Customer</label>
                <input v-model="editRowData.customer" type="text" class="form-control" id="editCustomer">
            </div>
            <div class="form-group">
                <label for="editOrder">Order</label>
                
                <select v-model="editRowData.order" class="form-control" id="editOrder">
                    <option value="antibiotics">antibiotics</option>
                    <option value="antibiotics">antibiotics</option>
                    <option value="antibiotics">antibiotics</option>
                    <option value="antibiotics">antibiotics</option>
                    <option value="antibiotics">antibiotics</option>
                    <option value="antibiotics">antibiotics</option>
                    
                   
                </select>
            </div>
            <div class="form-group">
                <label for="editDeliverDate">Deliver Date and Time</label>
                <input v-model="editRowData.deliveryDate" type="text" class="form-control" id="editDeliverDate">
            </div>

            <div class="form-group">
                <label for="orderPrice">Order Price</label>
                <input v-model="editRowData.orderPrice" type="text" class="form-control" id="orderPrice">
            </div>
            <div class="form-group">
                <label for="payment">Payment</label>
                
                <select v-model="editRowData.payment" class="form-control" id="payment">
                    <option value="Card">Card</option>
                    <option value="Bank Transfer">Bank Transfer</option>
                    <option value="Cash On Delivery">Cash On Delivery</option>
                    
                    
                </select>
            </div>
            <div class="form-group">
                <label for="editStatus">Status</label>
                <select v-model="editRowData.status" class="form-control" id="editStatus">
                    <option value="Pending">Pending</option>
                
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
                    <label for="orderid">OrderId</label>
                    <select v-model="newRow.orderid" class="form-control" id="orderid">
                        <option value="ASDR34R">ASDR34R</option>
                        <option value="ASDR35R">ASDR35R</option>
                        <option value="ASDR36R">ASDR36R</option>
                        <option value="ASDR37R">ASDR34R</option>
                        <option value="ASDR38R">ASDR38R</option>
                        <option value="ASDR39R">ASDR39R</option>
                 
                    </select>

                    
                
                </div>


                <div class="form-group">
                    <label for="customer">Customer</label>
                    <input v-model="newRow.customer" type="text" class="form-control" id="customer">
                </div>

                <div class="form-group">
                    <label for="addOrder">Order</label>
                    
                    <select v-model="newRow.order" class="form-control" id="addOrder">
                        <option value="antibiotics">antibiotics</option>
                        <option value="antibiotics">antibiotics</option>
                        <option value="antibiotics">antibiotics</option>
                        <option value="antibiotics">antibiotics</option>
                        <option value="antibiotics">antibiotics</option>
                        <option value="antibiotics">antibiotics</option>
                        
                        
                    </select>
                </div>

                <div class="form-group">
                    <label for="addDeliverDate">Deliver Date and Time</label>
                    <input v-model="newRow.deliveryDate" type="text" class="form-control" id="addDeliverDate">
                </div>

                <div class="form-group">
                    <label for="addclosingTime">Closing Time</label>
                    <input v-model="newRow.closingTime" type="text" class="form-control" id="addclosingTime">
                </div>

                <div class="form-group">
                    <label for="addorderPrice">Order Price</label>
                    <input v-model="newRow.orderPrice" type="text" class="form-control" id="addrderPrice">
                </div>
                <div class="form-group">
                    <label for="addpayment">Payment</label>
                    
                    <select v-model="newRow.payment" class="form-control" id="addpayment">
                        <option value="Card">Card</option>
                        <option value="Bank Transfer">Bank Transfer</option>
                        <option value="Cash On Delivery">Cash On Delivery</option>
                        
                        
                       
                    </select>
                </div>
              

                <div class="form-group">
                    <label for="status">Status</label>
                    <select v-model="newRow.status" class="form-control" id="status">
                        <option value="Pending">Pending</option>
                    
                    </select>
                </div>

                <b-button type="submit" variant="primary">Add</b-button>
                <b-button variant="secondary" @click="showAddModal = false">Cancel</b-button>
            -->
            </form>
        </b-modal>

        <!--Adding Chatbox-->
        <b-modal v-model="showPendingChart" size="lg">
            <PendingChart/>
        </b-modal>
    </div>
</template>


<script>
import { BModal, BButton } from "bootstrap-vue";
import PendingChart from './chart/pending.vue';

export default {
    name: 'pending',
    metaInfo: {
      // if no subcomponents specify a metaInfo.title, this title will be used
        title: "DropDown"
    },

  components: {
    // Register Bootstrap-Vue components
    BModal,
    BButton,
    PendingChart,
  },
  

  data() {
    return {

      showEditModal: false, // Control edit modal visibility
      editRowData: {}, // Data for the row being edited
      editRowIndex: -1, // Index of the row being edited
      showPendingChart: false, //Control chart modal visibility
      

      showAddModal: false, // Control modal visibility
      newRow: {
        orderid: "",
        customer: "",
        order: "",
        deliveryDate: "",
        orderPrice : "",
        status: "Pending",
        payment: "",
      },
      
      openingHours: [
        {
          id: 1,
          orderid: "ASDR34R",
          customer: "John Smith",
          order: "antibiotics",
          deliveryDate: "23-05-2014",
          orderPrice: "5000",
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
        orderid: "",
        customer: "",
        order: "",
        deliveryDate: "",
        orderPrice : "",
        status: "Pending",
        payment: "",
      };
      this.showAddModal = false;
    },
    addChatRow(){
      
      this.showPendingChart = true;
    }
    
    
    
  },
};
</script>