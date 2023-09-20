<template>
    <div class="main-content">
        
        <breadcumb :page="'Revenue Orders'" :folder="'Revenue'" :folder2="'Orders'" />
        <!--
        <b-row>
            <b-col md="4" class=" mb-30">
                <b-card class="h-100" title="Basic Examples" >
                    <b-dropdown variant="primary" id="dropdown-1" text="Dropdown Button" class="mb-2 ">
                        <b-dropdown-item>First Action</b-dropdown-item>
                        <b-dropdown-item>Second Action</b-dropdown-item>
                        <b-dropdown-item>Third Action</b-dropdown-item>
                        <b-dropdown-divider></b-dropdown-divider>
                        <b-dropdown-item active>Active action</b-dropdown-item>
                        <b-dropdown-item disabled>Disabled action</b-dropdown-item>
                    </b-dropdown>

                    <b-dropdown variant="primary" id="dropdown-1" text="Icon Menu" class="mb-2">
                        <b-dropdown-item>
                            <i class="i-Bell m-1"> </i>
                                First Action
                        </b-dropdown-item>
                        <b-dropdown-item>
                            <i class="i-Download-from-Cloud m-1"> </i>
                                Second Action
                        </b-dropdown-item>
                        <b-dropdown-item>
                            <i class="i-Money-Bag"> </i>
                            Third Action
                        </b-dropdown-item>
                        
                    </b-dropdown>
                </b-card>
            </b-col>
            <b-col md="4" class=" mb-30">
                <b-card class="h-100" title="Menu Alignment" >
                    <b-dropdown  id="dropdown-1" text="Dropdown Button" class="">
                        <b-dropdown-item>First Action</b-dropdown-item>
                        <b-dropdown-item>Second Action</b-dropdown-item>
                        <b-dropdown-item>Third Action</b-dropdown-item>
                        <b-dropdown-divider></b-dropdown-divider>
                        <b-dropdown-item active>Active action</b-dropdown-item>
                        <b-dropdown-item disabled>Disabled action</b-dropdown-item>
                    </b-dropdown>
                </b-card>
            </b-col>

            <b-col md="4" class="mb-30">
                <b-card class="h-100" title="Offset Dropdown">
                    <b-dropdown variant="danger" id="dropdown-offset" offset="25" text="Offset Dropdown" class="mb-2">
                        <b-dropdown-item href="#">Action</b-dropdown-item>
                        <b-dropdown-item href="#">Another action</b-dropdown-item>
                        <b-dropdown-item href="#">Something else here</b-dropdown-item>
                    </b-dropdown>
                </b-card>
            </b-col>
            <b-col md="4" class="mb-30">
                <b-card class="h-100" title="Dropup Variation">
                    <b-dropdown id="dropdown-dropup" dropup text="Drop-Up" variant="primary" class="mb-2">
                        <b-dropdown-item href="#">Action</b-dropdown-item>
                        <b-dropdown-item href="#">Another action</b-dropdown-item>
                        <b-dropdown-item href="#">Something else here</b-dropdown-item>
                    </b-dropdown>

                    <b-dropdown id="dropdown-dropright" dropright text="Drop-Right" variant="primary" class="mb-2">
                        <b-dropdown-item href="#">Action</b-dropdown-item>
                        <b-dropdown-item href="#">Another action</b-dropdown-item>
                        <b-dropdown-item href="#">Something else here</b-dropdown-item>
                    </b-dropdown>

                    <b-dropdown id="dropdown-dropleft" dropleft text="Drop-Left" variant="primary" class="mb-2">
                        <b-dropdown-item href="#">Action</b-dropdown-item>
                        <b-dropdown-item href="#">Another action</b-dropdown-item>
                        <b-dropdown-item href="#">Something else here</b-dropdown-item>
                    </b-dropdown>

                </b-card>
            </b-col>

            <b-col md="4" class="mb-30">
                <b-card class="h-100" title="Split Button Link">
                    <b-dropdown split split-href="#foo/bar" text="Split Link" class="mb-2">
                        <b-dropdown-item href="#">Action</b-dropdown-item>
                        <b-dropdown-item href="#">Another action</b-dropdown-item>
                        <b-dropdown-item href="#">Something else here...</b-dropdown-item>
                    </b-dropdown>
                </b-card>
            </b-col>

            <b-col md="4" class="mb-30">
                <b-card class="h-100" title="Dropdown Variant Color">
                    <div>
                        <b-dropdown text="Primary" variant="primary" class="mb-2">
                            <b-dropdown-item href="#">Action</b-dropdown-item>
                            <b-dropdown-item href="#">Another action</b-dropdown-item>
                            <b-dropdown-item href="#">Something else here</b-dropdown-item>
                        </b-dropdown>

                        <b-dropdown text="Success" variant="success" class="mb-2">
                            <b-dropdown-item href="#">Action</b-dropdown-item>
                            <b-dropdown-item href="#">Another action</b-dropdown-item>
                            <b-dropdown-item href="#">Something else here</b-dropdown-item>
                        </b-dropdown>

                        <b-dropdown text="Outline Danger" variant="outline-danger" class="mb-2">
                            <b-dropdown-item href="#">Action</b-dropdown-item>
                            <b-dropdown-item href="#">Another action</b-dropdown-item>
                            <b-dropdown-item href="#">Something else here</b-dropdown-item>
                        </b-dropdown>
                    </div>
                </b-card>
            </b-col>
            <b-col md="4" class="mb-30">
                <b-card class="h-100" title="Split button color variant">
                    <div>
                        <b-dropdown
                            split
                            split-variant="outline-primary"
                            variant="primary"
                            text=" Dropdown"
                            class="mb-3"
                        >
                            <b-dropdown-item href="#">Action</b-dropdown-item>
                            <b-dropdown-item href="#">Another action</b-dropdown-item>
                            <b-dropdown-item href="#">Something else here...</b-dropdown-item>
                        </b-dropdown>
                        <b-dropdown
                            split
                            split-variant="outline-info"
                            variant="primary"
                            text=" Dropdown"
                            class="mb-3"
                        >
                            <b-dropdown-item href="#">Action</b-dropdown-item>
                            <b-dropdown-item href="#">Another action</b-dropdown-item>
                            <b-dropdown-item href="#">Something else here...</b-dropdown-item>
                        </b-dropdown>
                    </div>
                </b-card>
            </b-col>
            <b-col md="4" class="mb-30">
                <b-card class="h-100" title="Icon Button">
                    <div>
                        <b-dropdown size="lg"  variant="link" toggle-class="text-decoration-none" no-caret>
                            <template slot="button-content">&#x1f50d;<span class="sr-only">Search</span></template>
                            <b-dropdown-item href="#">Action</b-dropdown-item>
                            <b-dropdown-item href="#">Another action</b-dropdown-item>
                            <b-dropdown-item href="#">Something else here...</b-dropdown-item>
                        </b-dropdown>
                    </div>
                </b-card>
            </b-col>

            <b-col md="4" class="mb-30">
                <b-card class="h-100" title="Dropdown Form">
                     <div>
                        <b-dropdown id="dropdown-form" text="Dropdown with form" ref="dropdown" class="mb-2">
                        <b-dropdown-form>
                            <b-form-group label="Email" label-for="dropdown-form-email" @submit.stop.prevent>
                            <b-form-input
                                id="dropdown-form-email"
                                size="sm"
                                placeholder="email@example.com"
                            ></b-form-input>
                            </b-form-group>

                            <b-form-group label="Password" label-for="dropdown-form-password">
                            <b-form-input
                                id="dropdown-form-password"
                                type="password"
                                size="sm"
                                placeholder="Password"
                            ></b-form-input>
                            </b-form-group>

                            <b-form-checkbox class="mb-3">Remember me</b-form-checkbox>
                            <b-button variant="primary" size="sm" @click="onClick">Sign In</b-button>
                        </b-dropdown-form>
                        <b-dropdown-divider></b-dropdown-divider>
                        <b-dropdown-item-button>New around here? Sign up</b-dropdown-item-button>
                        <b-dropdown-item-button>Forgot Password?</b-dropdown-item-button>
                        </b-dropdown>
                    </div>
                </b-card>
            </b-col>

            <b-col md="4" class="mb-30">
                <b-card class="h-100" title="Dropdown Group">
                    <div>
                        <b-dropdown id="dropdown-header" variant="info" text="Dropdown with group" class="mb-2">
                            <b-dropdown-item-button>
                            Non-grouped Item
                            </b-dropdown-item-button>
                            <b-dropdown-divider></b-dropdown-divider>
                            <b-dropdown-group id="dropdown-group-1" header="Group 1">
                            <b-dropdown-item-button>First Grouped item</b-dropdown-item-button>
                            <b-dropdown-item-button>Second Grouped Item</b-dropdown-item-button>
                            </b-dropdown-group>
                            <b-dropdown-group id="dropdown-group-2" header="Group 2">
                            <b-dropdown-item-button>First Grouped item</b-dropdown-item-button>
                            <b-dropdown-item-button>Second Grouped Item</b-dropdown-item-button>
                            </b-dropdown-group>
                            <b-dropdown-divider></b-dropdown-divider>
                            <b-dropdown-item-button>
                            Another Non-grouped Item
                            </b-dropdown-item-button>
                        </b-dropdown>
                    </div>
                </b-card>
            </b-col>

            <b-col md="8" class="mb-30">
                <b-card class="h-100" title="Sizing">
                     <b-dropdown size="lg" text="Large" class="mb-2">
                        <b-dropdown-item-button>Action</b-dropdown-item-button>
                        <b-dropdown-item-button>Another action</b-dropdown-item-button>
                        <b-dropdown-item-button>Something else here</b-dropdown-item-button>
                    </b-dropdown>

                    <b-dropdown size="lg" split text="Large Split" class="mb-2">
                        <b-dropdown-item-button>Action</b-dropdown-item-button>
                        <b-dropdown-item-button>Another action</b-dropdown-item-button>
                        <b-dropdown-item-button>Something else here...</b-dropdown-item-button>
                    </b-dropdown>

                    <b-dropdown size="sm" text="Small" class="mb-2">
                        <b-dropdown-item-button>Action</b-dropdown-item-button>
                        <b-dropdown-item-button>Another action</b-dropdown-item-button>
                        <b-dropdown-item-button>Something else here...</b-dropdown-item-button>
                    </b-dropdown>

                     <b-dropdown size="sm" split text="Small Split" class="mb-2">
                        <b-dropdown-item-button>Action</b-dropdown-item-button>
                        <b-dropdown-item-button>Another action</b-dropdown-item-button>
                        <b-dropdown-item-button>Something else here...</b-dropdown-item-button>
                    </b-dropdown>
                </b-card>
            </b-col>
        </b-row>
        -->
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
                        <b-tab title="All Order" active>
                            <allOrder/>
                        </b-tab>
                        <!-- Edit Table Row Modal -->
                        
                        <b-tab title="Pending">
                            <pending/>
                        </b-tab>
                        <b-tab title="Packaged" >
                            <packaged/>
                        </b-tab>
                        <b-tab title="Completed">
                            <completed/>
                        </b-tab>
                        <b-tab title="Canceled">
                            <canceled/>
                        </b-tab>
                        <b-tab title="Restituted" >
                            <restituted/>
                        </b-tab>
                    </b-tabs>         
                </b-card> 
            </b-col>
        </div>
    </div>
</template>

<script>
import allOrder from './businessTable/allOrder.vue';
import pending from './businessTable/pending.vue';
import packaged from './businessTable/packaged.vue';
import completed from './businessTable/completed.vue';
import canceled from './businessTable/canceled.vue';
import restituted from './businessTable/restituted.vue';

export default {
    metaInfo: {
      // if no subcomponents specify a metaInfo.title, this title will be used
        title: "DropDown"
    },

  components: {
    // Register Bootstrap-Vue components
    allOrder,
    pending,
    packaged,
    completed,
    canceled,
    restituted,
  }
  

  
};
</script>