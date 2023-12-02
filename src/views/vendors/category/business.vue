<template>
  <div class="main-content">
    <breadcumb :page="'Business Hours'" :folder="'Business'" :folder2="'Hours'" />

    <div class="row">
      <div class="col-md-12 mb-3">
        <div class="card text-left">
          <div style="display: flex; justify-content:space-between;align-items:center; background-color:#fff;" class="p-3 rounded text-center">
            <h4 class="card-title mb-3">Opening Days/Time </h4>
            
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
                        <th scope="col">Days</th>
                        <th scope="col">Opening Time</th>
                        <th scope="col">Closing Time</th>
                        <th scope="col">Status</th>
                        <th scope="col">Action</th>
                      </tr>
                    </thead>
                    <tbody style="text-align:center;">
                      <tr v-for="(day, index) in openingHours" :key="day.id">
                        <th scope="row">{{ index + 1 }}</th>
                        <td>{{ day.name }}</td>
                        <td>{{ day.openingTime }}</td>
                        <td>{{ day.closingTime }}</td>
                        <td>
                          <span :class="day.status === 'Open' ? 'badge badge-success' : 'badge badge-danger'">
                            {{ day.status }}
                          </span>
                        </td>
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
          <label for="editDay">Day</label>
          <select v-model="editRowData.name" class="form-control" id="editDay">
            <option value="Monday">Monday</option>
            <option value="Tueday">Tuesday</option>
            <option value="Wednesday">Wednesday</option>
            <option value="Thursday">Thursday</option>
            <option value="Friday">Friday</option>
            <option value="Saturday">Saturday</option>
            <option value="Sunday">Sunday</option>
           
          </select>
        </div>
        <div class="form-group">
          <label for="editOpeningTime">Opening Time</label>
          <input v-model="editRowData.openingTime" type="text" class="form-control" id="editOpeningTime">
        </div>
        <div class="form-group">
          <label for="editClosingTime">Closing Time</label>
          <input v-model="editRowData.closingTime" type="text" class="form-control" id="editClosingTime">
        </div>
        <div class="form-group">
          <label for="editStatus">Status</label>
          <select v-model="editRowData.status" class="form-control" id="editStatus">
            <option value="Open">Open</option>
            <option value="Closed">Closed</option>
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
          <label for="day">Day</label>
          <select v-model="newRow.name" class="form-control" id="day">
            <option value="Monday">Monday</option>
            <option value="Tueday">Tuesday</option>
            <option value="Wednesday">Wednesday</option>
            <option value="Thursday">Thursday</option>
            <option value="Friday">Friday</option>
            <option value="Saturday">Saturday</option>
            <option value="Sunday">Sunday</option>
            
          </select>
        </div>
        <div class="form-group">
          <label for="openingTime">Opening Time</label>
          <input v-model="newRow.openingTime" type="text" class="form-control" id="openingTime">
        </div>
        <div class="form-group">
          <label for="closingTime">Closing Time</label>
          <input v-model="newRow.closingTime" type="text" class="form-control" id="closingTime">
        </div>
        <div class="form-group">
          <label for="status">Status</label>
          <select v-model="newRow.status" class="form-control" id="status">
            <option value="Open">Open</option>
            <option value="Closed">Closed</option>
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
        name: "",
        openingTime: "",
        closingTime: "",
        status: "Open",
      },
      
      openingHours: [
        {
          id: 1,
          name: "Monday",
          openingTime: "9:00 am",
          closingTime: "5:00 pm",
          status: "Open"
        },
        {
          id: 2,
          name: "Tuesday",
          openingTime: "9:00 am",
          closingTime: "5:00 pm",
          status: "Open"
        },
        {
          id: 3,
          name: "Wednesday",
          openingTime: "9:00 am",
          closingTime: "5:00 pm",
          status: "Open"
        },
        {
          id: 4,
          name: "Thursday",
          openingTime: "9:00 am",
          closingTime: "5:00 pm",
          status: "Open"
        },
        {
          id: 5,
          name: "Friday",
          openingTime: "9:00 am",
          closingTime: "5:00 pm",
          status: "Closed"
        },
        {
          id: 6,
          name: "Saturday",
          openingTime: "9:00 am",
          closingTime: "5:00 pm",
          status: "Closed"
        },
        {
          id: 7,
          name: "Sunday",
          openingTime: "9:00 am",
          closingTime: "5:00 pm",
          status: "Closed"
        }
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
        name: "",
        openingTime: "",
        closingTime: "",
        status: "Open",
      };
      this.showAddModal = false;
    }
    
    
  },
};
</script>
  