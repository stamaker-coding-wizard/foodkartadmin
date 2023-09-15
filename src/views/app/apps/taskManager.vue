<template>
    <div class="main-content">
        
        <breadcumb :page="'Revenue Orders'" :folder="'Revenue'" :folder2="'Order'" />
       

        <!-- content-start -->
        <!--
        <b-row>
            <b-col md="9">
                <b-row>
                    <b-col xl="6">
                        <b-card class=" mb-30">
                            <div class="d-sm-flex align-item-sm-center flex-sm-nowrap">
                                            <div>
                                                <h5><a href="">#23. New icons set for an iOS app</a></h5>
                                                <p class="ul-task-manager__paragraph mb-3">A collection of textile samples ..</p>

                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle " width="36" height="36" alt="corrupted">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle" width="36" height="36" alt="corrupted 2">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle" width="36" height="36" alt="corrupted 2">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <i class="ul-task-manager__fonts i-Add text-30 " style="vertical-align:middle"></i>
                                                </a>
                                                <a href="" class="btn btn-icon bg-transparent border-slate-300 text-slate rounded-round border-dashed"><i class="icon-plus22"></i></a>
                                            </div>

                                            <ul class="list list-unstyled mb-0 mt-3 mt-sm-0 ml-auto">
                                                <li><span class="ul-task-manager__font-date text-muted">20 Jan,2015</span></li>
                                                <li class="dropdown">
                                                    Priority: &nbsp;
                                                    <a href="#" class="badge badge-danger align-top dropdown-toggle" data-toggle="dropdown">Blocker</a>
                                                    <div class="dropdown-menu dropdown-menu-right">
                                                        <a href="#" class="dropdown-item active"><span class="badge badge-mark mr-2 border-danger"></span> Blocker</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-warning-400"></span> High priority</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-success"></span> Normal priority</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-grey-300"></span> Low priority</a>
                                                    </div>
                                                </li> 
                                                <li><a href="#">Eternity app</a></li>
                                            </ul>
                                        </div>
                                     <div slot="footer">
                                        <small class="text-muted d-sm-flex justify-content-sm-between align-items-sm-center">
                                            <span>Due: <span class="font-weight-semibold">18 hours</span></span>
                                            
                                            

                                            
                                            <div class="list-inline mb-0 mt-2 mt-sm-0">
                                                <b-dropdown  variant="link p-0" toggle-class="text-decoration-none" no-caret>
                                                    <template slot="button-content">On hold</template>
                                                    <b-dropdown-item href="#">Action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Another action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Something else here...</b-dropdown-item>
                                                </b-dropdown>

                                                <b-dropdown  variant="link p-2" toggle-class="text-decoration-none" no-caret>
                                                    <template slot="button-content"><i class="i-Gear-2"></i></template>
                                                    <b-dropdown-item href="#">Action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Another action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Something else here...</b-dropdown-item>
                                                </b-dropdown>
                                            </div>
                                        </small>
                                    </div>     
                                        
                        </b-card>
                    </b-col>
                    <b-col xl="6">
                        <b-card class=" mb-30">
                            <div class="d-sm-flex align-item-sm-center flex-sm-nowrap">
                                            <div>
                                                <h5><a href="">#23. New icons set for an iOS app</a></h5>
                                                <p class="ul-task-manager__paragraph mb-3">A collection of textile samples ..</p>

                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle " width="36" height="36" alt="corrupted">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle" width="36" height="36" alt="corrupted 2">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle" width="36" height="36" alt="corrupted 2">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <i class="ul-task-manager__fonts i-Add text-30 " style="vertical-align:middle"></i>
                                                </a>
                                                <a href="" class="btn btn-icon bg-transparent border-slate-300 text-slate rounded-round border-dashed"><i class="icon-plus22"></i></a>
                                            </div>

                                            <ul class="list list-unstyled mb-0 mt-3 mt-sm-0 ml-auto">
                                                <li><span class="ul-task-manager__font-date text-muted">20 Jan,2015</span></li>
                                                 <li class="dropdown">
                                                    Priority: &nbsp;
                                                    <a href="#" class="badge badge-danger align-top dropdown-toggle" data-toggle="dropdown">Blocker</a>
                                                    <div class="dropdown-menu dropdown-menu-right">
                                                        <a href="#" class="dropdown-item active"><span class="badge badge-mark mr-2 border-danger"></span> Blocker</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-warning-400"></span> High priority</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-success"></span> Normal priority</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-grey-300"></span> Low priority</a>
                                                    </div>
                                                </li> 
                                                <li><a href="#">Eternity app</a></li>
                                            </ul>
                                        </div>
                                     <div slot="footer">
                                        <small class="text-muted d-sm-flex justify-content-sm-between align-items-sm-center">
                                            <span>Due: <span class="font-weight-semibold">18 hours</span></span>
                                            
                                            

                                            
                                            <div class="list-inline mb-0 mt-2 mt-sm-0">
                                                <b-dropdown  variant="link p-0" toggle-class="text-decoration-none" no-caret>
                                                    <template slot="button-content">On hold</template>
                                                    <b-dropdown-item href="#">Action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Another action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Something else here...</b-dropdown-item>
                                                </b-dropdown>

                                                <b-dropdown  variant="link p-2" toggle-class="text-decoration-none" no-caret>
                                                    <template slot="button-content"><i class="i-Gear-2"></i></template>
                                                    <b-dropdown-item href="#">Action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Another action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Something else here...</b-dropdown-item>
                                                </b-dropdown>
                                            </div>
                                        </small>
                                    </div>     
                                        
                        </b-card>
                    </b-col>
                    <b-col xl="6">
                        <b-card class=" mb-30">
                            <div class="d-sm-flex align-item-sm-center flex-sm-nowrap">
                                            <div>
                                                <h5><a href="">#23. New icons set for an iOS app</a></h5>
                                                <p class="ul-task-manager__paragraph mb-3">A collection of textile samples ..</p>

                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle " width="36" height="36" alt="corrupted">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle" width="36" height="36" alt="corrupted 2">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle" width="36" height="36" alt="corrupted 2">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <i class="ul-task-manager__fonts i-Add text-30 " style="vertical-align:middle"></i>
                                                </a>
                                                <a href="" class="btn btn-icon bg-transparent border-slate-300 text-slate rounded-round border-dashed"><i class="icon-plus22"></i></a>
                                            </div>

                                            <ul class="list list-unstyled mb-0 mt-3 mt-sm-0 ml-auto">
                                                <li><span class="ul-task-manager__font-date text-muted">20 Jan,2015</span></li>
                                                 <li class="dropdown">
                                                    Priority: &nbsp;
                                                    <a href="#" class="badge badge-danger align-top dropdown-toggle" data-toggle="dropdown">Blocker</a>
                                                    <div class="dropdown-menu dropdown-menu-right">
                                                        <a href="#" class="dropdown-item active"><span class="badge badge-mark mr-2 border-danger"></span> Blocker</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-warning-400"></span> High priority</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-success"></span> Normal priority</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-grey-300"></span> Low priority</a>
                                                    </div>
                                                </li> 
                                                <li><a href="#">Eternity app</a></li>
                                            </ul>
                                        </div>
                                     <div slot="footer">
                                        <small class="text-muted d-sm-flex justify-content-sm-between align-items-sm-center">
                                            <span>Due: <span class="font-weight-semibold">18 hours</span></span>
                                            
                                            

                                            
                                            <div class="list-inline mb-0 mt-2 mt-sm-0">
                                                <b-dropdown  variant="link p-0" toggle-class="text-decoration-none" no-caret>
                                                    <template slot="button-content">On hold</template>
                                                    <b-dropdown-item href="#">Action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Another action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Something else here...</b-dropdown-item>
                                                </b-dropdown>

                                                <b-dropdown  variant="link p-2" toggle-class="text-decoration-none" no-caret>
                                                    <template slot="button-content"><i class="i-Gear-2"></i></template>
                                                    <b-dropdown-item href="#">Action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Another action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Something else here...</b-dropdown-item>
                                                </b-dropdown>
                                            </div>
                                        </small>
                                    </div>     
                                        
                        </b-card>
                    </b-col>
                    <b-col xl="6">
                        <b-card class=" mb-30">
                            <div class="d-sm-flex align-item-sm-center flex-sm-nowrap">
                                            <div>
                                                <h5><a href="">#23. New icons set for an iOS app</a></h5>
                                                <p class="ul-task-manager__paragraph mb-3">A collection of textile samples ..</p>

                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle " width="36" height="36" alt="corrupted">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle" width="36" height="36" alt="corrupted 2">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle" width="36" height="36" alt="corrupted 2">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <i class="ul-task-manager__fonts i-Add text-30 " style="vertical-align:middle"></i>
                                                </a>
                                                <a href="" class="btn btn-icon bg-transparent border-slate-300 text-slate rounded-round border-dashed"><i class="icon-plus22"></i></a>
                                            </div>

                                            <ul class="list list-unstyled mb-0 mt-3 mt-sm-0 ml-auto">
                                                <li><span class="ul-task-manager__font-date text-muted">20 Jan,2015</span></li>
                                                 <li class="dropdown">
                                                    Priority: &nbsp;
                                                    <a href="#" class="badge badge-danger align-top dropdown-toggle" data-toggle="dropdown">Blocker</a>
                                                    <div class="dropdown-menu dropdown-menu-right">
                                                        <a href="#" class="dropdown-item active"><span class="badge badge-mark mr-2 border-danger"></span> Blocker</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-warning-400"></span> High priority</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-success"></span> Normal priority</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-grey-300"></span> Low priority</a>
                                                    </div>
                                                </li> 
                                                <li><a href="#">Eternity app</a></li>
                                            </ul>
                                        </div>
                                     <div slot="footer">
                                        <small class="text-muted d-sm-flex justify-content-sm-between align-items-sm-center">
                                            <span>Due: <span class="font-weight-semibold">18 hours</span></span>
                                            
                                            

                                            
                                            <div class="list-inline mb-0 mt-2 mt-sm-0">
                                                <b-dropdown  variant="link p-0" toggle-class="text-decoration-none" no-caret>
                                                    <template slot="button-content">On hold</template>
                                                    <b-dropdown-item href="#">Action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Another action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Something else here...</b-dropdown-item>
                                                </b-dropdown>

                                                <b-dropdown  variant="link p-2" toggle-class="text-decoration-none" no-caret>
                                                    <template slot="button-content"><i class="i-Gear-2"></i></template>
                                                    <b-dropdown-item href="#">Action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Another action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Something else here...</b-dropdown-item>
                                                </b-dropdown>
                                            </div>
                                        </small>
                                    </div>     
                                        
                        </b-card>
                    </b-col>
                    <b-col xl="6">
                        <b-card class=" mb-30">
                            <div class="d-sm-flex align-item-sm-center flex-sm-nowrap">
                                            <div>
                                                <h5><a href="">#23. New icons set for an iOS app</a></h5>
                                                <p class="ul-task-manager__paragraph mb-3">A collection of textile samples ..</p>

                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle " width="36" height="36" alt="corrupted">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle" width="36" height="36" alt="corrupted 2">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle" width="36" height="36" alt="corrupted 2">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <i class="ul-task-manager__fonts i-Add text-30 " style="vertical-align:middle"></i>
                                                </a>
                                                <a href="" class="btn btn-icon bg-transparent border-slate-300 text-slate rounded-round border-dashed"><i class="icon-plus22"></i></a>
                                            </div>

                                            <ul class="list list-unstyled mb-0 mt-3 mt-sm-0 ml-auto">
                                                <li><span class="ul-task-manager__font-date text-muted">20 Jan,2015</span></li>
                                                 <li class="dropdown">
                                                    Priority: &nbsp;
                                                    <a href="#" class="badge badge-danger align-top dropdown-toggle" data-toggle="dropdown">Blocker</a>
                                                    <div class="dropdown-menu dropdown-menu-right">
                                                        <a href="#" class="dropdown-item active"><span class="badge badge-mark mr-2 border-danger"></span> Blocker</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-warning-400"></span> High priority</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-success"></span> Normal priority</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-grey-300"></span> Low priority</a>
                                                    </div>
                                                </li> 
                                                <li><a href="#">Eternity app</a></li>
                                            </ul>
                                        </div>
                                     <div slot="footer">
                                        <small class="text-muted d-sm-flex justify-content-sm-between align-items-sm-center">
                                            <span>Due: <span class="font-weight-semibold">18 hours</span></span>
                                            
                                            

                                            
                                            <div class="list-inline mb-0 mt-2 mt-sm-0">
                                                <b-dropdown  variant="link p-0" toggle-class="text-decoration-none" no-caret>
                                                    <template slot="button-content">On hold</template>
                                                    <b-dropdown-item href="#">Action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Another action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Something else here...</b-dropdown-item>
                                                </b-dropdown>

                                                <b-dropdown  variant="link p-2" toggle-class="text-decoration-none" no-caret>
                                                    <template slot="button-content"><i class="i-Gear-2"></i></template>
                                                    <b-dropdown-item href="#">Action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Another action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Something else here...</b-dropdown-item>
                                                </b-dropdown>
                                            </div>
                                        </small>
                                    </div>     
                                        
                        </b-card>
                    </b-col>
                    <b-col xl="6">
                        <b-card class=" mb-30">
                            <div class="d-sm-flex align-item-sm-center flex-sm-nowrap">
                                            <div>
                                                <h5><a href="">#23. New icons set for an iOS app</a></h5>
                                                <p class="ul-task-manager__paragraph mb-3">A collection of textile samples ..</p>

                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle " width="36" height="36" alt="corrupted">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle" width="36" height="36" alt="corrupted 2">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle" width="36" height="36" alt="corrupted 2">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <i class="ul-task-manager__fonts i-Add text-30 " style="vertical-align:middle"></i>
                                                </a>
                                                <a href="" class="btn btn-icon bg-transparent border-slate-300 text-slate rounded-round border-dashed"><i class="icon-plus22"></i></a>
                                            </div>

                                            <ul class="list list-unstyled mb-0 mt-3 mt-sm-0 ml-auto">
                                                <li><span class="ul-task-manager__font-date text-muted">20 Jan,2015</span></li>
                                                 <li class="dropdown">
                                                    Priority: &nbsp;
                                                    <a href="#" class="badge badge-danger align-top dropdown-toggle" data-toggle="dropdown">Blocker</a>
                                                    <div class="dropdown-menu dropdown-menu-right">
                                                        <a href="#" class="dropdown-item active"><span class="badge badge-mark mr-2 border-danger"></span> Blocker</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-warning-400"></span> High priority</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-success"></span> Normal priority</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-grey-300"></span> Low priority</a>
                                                    </div>
                                                </li> 
                                                <li><a href="#">Eternity app</a></li>
                                            </ul>
                                        </div>
                                     <div slot="footer">
                                        <small class="text-muted d-sm-flex justify-content-sm-between align-items-sm-center">
                                            <span>Due: <span class="font-weight-semibold">18 hours</span></span>
                                            
                                            

                                            
                                            <div class="list-inline mb-0 mt-2 mt-sm-0">
                                                <b-dropdown  variant="link p-0" toggle-class="text-decoration-none" no-caret>
                                                    <template slot="button-content">On hold</template>
                                                    <b-dropdown-item href="#">Action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Another action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Something else here...</b-dropdown-item>
                                                </b-dropdown>

                                                <b-dropdown  variant="link p-2" toggle-class="text-decoration-none" no-caret>
                                                    <template slot="button-content"><i class="i-Gear-2"></i></template>
                                                    <b-dropdown-item href="#">Action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Another action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Something else here...</b-dropdown-item>
                                                </b-dropdown>
                                            </div>
                                        </small>
                                    </div>     
                                        
                        </b-card>
                    </b-col>
                    <b-col xl="6">
                        <b-card class=" mb-30">
                            <div class="d-sm-flex align-item-sm-center flex-sm-nowrap">
                                            <div>
                                                <h5><a href="">#23. New icons set for an iOS app</a></h5>
                                                <p class="ul-task-manager__paragraph mb-3">A collection of textile samples ..</p>

                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle " width="36" height="36" alt="corrupted">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle" width="36" height="36" alt="corrupted 2">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle" width="36" height="36" alt="corrupted 2">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <i class="ul-task-manager__fonts i-Add text-30 " style="vertical-align:middle"></i>
                                                </a>
                                                <a href="" class="btn btn-icon bg-transparent border-slate-300 text-slate rounded-round border-dashed"><i class="icon-plus22"></i></a>
                                            </div>

                                            <ul class="list list-unstyled mb-0 mt-3 mt-sm-0 ml-auto">
                                                <li><span class="ul-task-manager__font-date text-muted">20 Jan,2015</span></li>
                                                 <li class="dropdown">
                                                    Priority: &nbsp;
                                                    <a href="#" class="badge badge-danger align-top dropdown-toggle" data-toggle="dropdown">Blocker</a>
                                                    <div class="dropdown-menu dropdown-menu-right">
                                                        <a href="#" class="dropdown-item active"><span class="badge badge-mark mr-2 border-danger"></span> Blocker</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-warning-400"></span> High priority</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-success"></span> Normal priority</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-grey-300"></span> Low priority</a>
                                                    </div>
                                                </li> 
                                                <li><a href="#">Eternity app</a></li>
                                            </ul>
                                        </div>
                                     <div slot="footer">
                                        <small class="text-muted d-sm-flex justify-content-sm-between align-items-sm-center">
                                            <span>Due: <span class="font-weight-semibold">18 hours</span></span>
                                            
                                            

                                            
                                            <div class="list-inline mb-0 mt-2 mt-sm-0">
                                                <b-dropdown  variant="link p-0" toggle-class="text-decoration-none" no-caret>
                                                    <template slot="button-content">On hold</template>
                                                    <b-dropdown-item href="#">Action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Another action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Something else here...</b-dropdown-item>
                                                </b-dropdown>

                                                <b-dropdown  variant="link p-2" toggle-class="text-decoration-none" no-caret>
                                                    <template slot="button-content"><i class="i-Gear-2"></i></template>
                                                    <b-dropdown-item href="#">Action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Another action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Something else here...</b-dropdown-item>
                                                </b-dropdown>
                                            </div>
                                        </small>
                                    </div>     
                                        
                        </b-card>
                    </b-col>
                    <b-col xl="6">
                        <b-card class=" mb-30">
                            <div class="d-sm-flex align-item-sm-center flex-sm-nowrap">
                                            <div>
                                                <h5><a href="">#23. New icons set for an iOS app</a></h5>
                                                <p class="ul-task-manager__paragraph mb-3">A collection of textile samples ..</p>

                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle " width="36" height="36" alt="corrupted">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle" width="36" height="36" alt="corrupted 2">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle" width="36" height="36" alt="corrupted 2">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <i class="ul-task-manager__fonts i-Add text-30 " style="vertical-align:middle"></i>
                                                </a>
                                                <a href="" class="btn btn-icon bg-transparent border-slate-300 text-slate rounded-round border-dashed"><i class="icon-plus22"></i></a>
                                            </div>

                                            <ul class="list list-unstyled mb-0 mt-3 mt-sm-0 ml-auto">
                                                <li><span class="ul-task-manager__font-date text-muted">20 Jan,2015</span></li>
                                                 <li class="dropdown">
                                                    Priority: &nbsp;
                                                    <a href="#" class="badge badge-danger align-top dropdown-toggle" data-toggle="dropdown">Blocker</a>
                                                    <div class="dropdown-menu dropdown-menu-right">
                                                        <a href="#" class="dropdown-item active"><span class="badge badge-mark mr-2 border-danger"></span> Blocker</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-warning-400"></span> High priority</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-success"></span> Normal priority</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-grey-300"></span> Low priority</a>
                                                    </div>
                                                </li> 
                                                <li><a href="#">Eternity app</a></li>
                                            </ul>
                                        </div>
                                     <div slot="footer">
                                        <small class="text-muted d-sm-flex justify-content-sm-between align-items-sm-center">
                                            <span>Due: <span class="font-weight-semibold">18 hours</span></span>
                                            
                                            

                                            
                                            <div class="list-inline mb-0 mt-2 mt-sm-0">
                                                <b-dropdown  variant="link p-0" toggle-class="text-decoration-none" no-caret>
                                                    <template slot="button-content">On hold</template>
                                                    <b-dropdown-item href="#">Action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Another action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Something else here...</b-dropdown-item>
                                                </b-dropdown>

                                                <b-dropdown  variant="link p-2" toggle-class="text-decoration-none" no-caret>
                                                    <template slot="button-content"><i class="i-Gear-2"></i></template>
                                                    <b-dropdown-item href="#">Action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Another action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Something else here...</b-dropdown-item>
                                                </b-dropdown>
                                            </div>
                                        </small>
                                    </div>     
                                        
                        </b-card>
                    </b-col>
                    <b-col xl="6">
                        <b-card class=" mb-30">
                            <div class="d-sm-flex align-item-sm-center flex-sm-nowrap">
                                            <div>
                                                <h5><a href="">#23. New icons set for an iOS app</a></h5>
                                                <p class="ul-task-manager__paragraph mb-3">A collection of textile samples ..</p>

                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle " width="36" height="36" alt="corrupted">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle" width="36" height="36" alt="corrupted 2">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle" width="36" height="36" alt="corrupted 2">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <i class="ul-task-manager__fonts i-Add text-30 " style="vertical-align:middle"></i>
                                                </a>
                                                <a href="" class="btn btn-icon bg-transparent border-slate-300 text-slate rounded-round border-dashed"><i class="icon-plus22"></i></a>
                                            </div>

                                            <ul class="list list-unstyled mb-0 mt-3 mt-sm-0 ml-auto">
                                                <li><span class="ul-task-manager__font-date text-muted">20 Jan,2015</span></li>
                                                 <li class="dropdown">
                                                    Priority: &nbsp;
                                                    <a href="#" class="badge badge-danger align-top dropdown-toggle" data-toggle="dropdown">Blocker</a>
                                                    <div class="dropdown-menu dropdown-menu-right">
                                                        <a href="#" class="dropdown-item active"><span class="badge badge-mark mr-2 border-danger"></span> Blocker</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-warning-400"></span> High priority</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-success"></span> Normal priority</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-grey-300"></span> Low priority</a>
                                                    </div>
                                                </li> 
                                                <li><a href="#">Eternity app</a></li>
                                            </ul>
                                        </div>
                                     <div slot="footer">
                                        <small class="text-muted d-sm-flex justify-content-sm-between align-items-sm-center">
                                            <span>Due: <span class="font-weight-semibold">18 hours</span></span>
                                            
                                            

                                            
                                            <div class="list-inline mb-0 mt-2 mt-sm-0">
                                                <b-dropdown  variant="link p-0" toggle-class="text-decoration-none" no-caret>
                                                    <template slot="button-content">On hold</template>
                                                    <b-dropdown-item href="#">Action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Another action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Something else here...</b-dropdown-item>
                                                </b-dropdown>

                                                <b-dropdown  variant="link p-2" toggle-class="text-decoration-none" no-caret>
                                                    <template slot="button-content"><i class="i-Gear-2"></i></template>
                                                    <b-dropdown-item href="#">Action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Another action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Something else here...</b-dropdown-item>
                                                </b-dropdown>
                                            </div>
                                        </small>
                                    </div>     
                                        
                        </b-card>
                    </b-col>
                    <b-col xl="6">
                        <b-card class=" mb-30">
                            <div class="d-sm-flex align-item-sm-center flex-sm-nowrap">
                                            <div>
                                                <h5><a href="">#23. New icons set for an iOS app</a></h5>
                                                <p class="ul-task-manager__paragraph mb-3">A collection of textile samples ..</p>

                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle " width="36" height="36" alt="corrupted">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle" width="36" height="36" alt="corrupted 2">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <img src="@/assets/images/faces/1.jpg" class="rounded-circle" width="36" height="36" alt="corrupted 2">
                                                </a>
                                                <a href="#" class="m-1">
                                                    <i class="ul-task-manager__fonts i-Add text-30 " style="vertical-align:middle"></i>
                                                </a>
                                                <a href="" class="btn btn-icon bg-transparent border-slate-300 text-slate rounded-round border-dashed"><i class="icon-plus22"></i></a>
                                            </div>

                                            <ul class="list list-unstyled mb-0 mt-3 mt-sm-0 ml-auto">
                                                <li><span class="ul-task-manager__font-date text-muted">20 Jan,2015</span></li>
                                                <li class="dropdown">
                                                    Priority: &nbsp;
                                                    <a href="#" class="badge badge-danger align-top dropdown-toggle" data-toggle="dropdown">Blocker</a>
                                                    <div class="dropdown-menu dropdown-menu-right">
                                                        <a href="#" class="dropdown-item active"><span class="badge badge-mark mr-2 border-danger"></span> Blocker</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-warning-400"></span> High priority</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-success"></span> Normal priority</a>
                                                        <a href="#" class="dropdown-item"><span class="badge badge-mark mr-2 border-grey-300"></span> Low priority</a>
                                                    </div>
                                                </li> 
                                                <li><a href="#">Eternity app</a></li>
                                            </ul>
                                        </div>
                                     <div slot="footer">
                                        <small class="text-muted d-sm-flex justify-content-sm-between align-items-sm-center">
                                            <span>Due: <span class="font-weight-semibold">18 hours</span></span>
                                            
                                            

                                            
                                            <div class="list-inline mb-0 mt-2 mt-sm-0">
                                                <b-dropdown  variant="link p-0" toggle-class="text-decoration-none" no-caret>
                                                    <template slot="button-content">On hold</template>
                                                    <b-dropdown-item href="#">Action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Another action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Something else here...</b-dropdown-item>
                                                </b-dropdown>

                                                <b-dropdown  variant="link p-2" toggle-class="text-decoration-none" no-caret>
                                                    <template slot="button-content"><i class="i-Gear-2"></i></template>
                                                    <b-dropdown-item href="#">Action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Another action</b-dropdown-item>
                                                    <b-dropdown-item href="#">Something else here...</b-dropdown-item>
                                                </b-dropdown>
                                            </div>
                                        </small>
                                    </div>     
                                        
                        </b-card>
                    </b-col>

                    
                   
                </b-row>
            </b-col>
            
            <b-col md="3">
    
               
                <b-row>-->
                     <!-- search -->
                     <!--
                    <b-col md="12">
                        <b-card  
                            b-card-link
                            no-body
                            class="mb-30  o-hidden">
                            <b-card-header 
                                style="cursor:pointer"
                                v-b-toggle.collapse-1>
                                Search Task
                            </b-card-header>
                            <b-collapse 
                                visible 
                                id="collapse-1" 
                                class="mt-2">
                                <b-card-body>
                                    <input type="text" placeholder="type  &amp;  hit enter" class="form-control">
                                </b-card-body>
                                    
                                
                            </b-collapse>
                        </b-card>
                    </b-col>-->
                 

                    <!-- navigation -->
                    <!--
                    <b-col md="12">
                        <b-card  
                            b-card-link
                            no-body
                            class="mb-30  o-hidden">-->
                            <!-- <b-card-header 
                                 style="cursor:pointer"
                                v-b-toggle.collapse-3>
                                Navigation
                            </b-card-header> -->
                            <!--
                            <b-collapse 
                                visible 
                                id="collapse-3" 
                                class="mt-2">
                                <b-card-body>
                                    <p class="card-text">Actions</p>
                                    <b-list-group>
                                        <b-list-group-item button>
                                            <a href=""><i class="i-Empty-Box mr-2"> </i> Create Project</a>
                                        </b-list-group-item>
                                        <b-list-group-item button>
                                            <a href=""><i class="i-Edit mr-2"> </i>  Edit Task List</a>
                                        </b-list-group-item>
                                        <b-list-group-item button>
                                            <a href=""><i class="i-Add-User mr-2"> </i>  Assign User</a>
                                        </b-list-group-item>
                                        <b-list-group-item button>
                                            <a href=""><i class="i-Network mr-2"> </i>  Create Team </a>
                                        </b-list-group-item>
                                        
                                    </b-list-group>

                                    <div class=" mb-30"></div>

                                    <p class="card-text">Tasks</p>

                                    <b-list-group>
                                        <b-list-group-item button>
                                            <a href=""><i class="i-Folders mr-2"> </i> All Tasks</a>
                                        </b-list-group-item>
                                        <b-list-group-item button>
                                            <a href=""><i class="i-Add-File mr-2"> </i> Active Tasks</a>
                                        </b-list-group-item>
                                        <b-list-group-item button>
                                            <a href=""><i class="i-File-Favorite mr-2"> </i> Closed Tasks</a>
                                        </b-list-group-item>
                                        <b-list-group-item button>
                                            <a href=""><i class="i-Administrator mr-2"> </i>  Assigned To Me  
                                                  <b-badge pill variant="primary ml-4">14</b-badge>
                                             </a>
                                        </b-list-group-item>
                                        <b-list-group-item button>
                                            <a href=""><i class="i-Conference mr-2"> </i>   Assigned To My Team    
                                                  <b-badge pill variant="primary ml-4">14</b-badge>
                                             </a>
                                        </b-list-group-item>
                                        <b-list-group-item button>
                                            <a href=""><i class="i-Gears mr-2"> </i> Settings     
                                                  
                                             </a>
                                        </b-list-group-item>
                                        
                                    </b-list-group>
                                </b-card-body>                             
                            </b-collapse>
                            </b-card>
                    </b-col>-->
                    
                    <!-- assigners -->
                    <!--

                    <b-col md="12">
                             <b-card  
                            b-card-link
                            no-body
                            class="mb-30  o-hidden">
                            <b-card-header 
                                style="cursor:pointer"
                                v-b-toggle.collapse-4>
                                Assigners
                            </b-card-header>
                            <b-collapse 
                                visible 
                                id="collapse-4" 
                                class="mt-2">
                                <b-card-body>
                                    <ul class="media-list pl-0">
                                        <li class="media mb-4">
                                            <a href="#" class="mr-4">
                                                <img src="http://gull-html-laravel.ui-lib.com/assets/images/faces/1.jpg" class="rounded-circle" width="40" alt="asd" srcset="">
                                            </a>
                                            <div class="ul-task-manager__media">
                                                <a href="">James Alexander gull</a>
                                                <div class="font-size-sm text-muted">Santa Ana,CA</div>
                                            </div>
                                            <div class="ml-3 align-self-center">
                                                <span class="badge badge-mark"></span>
                                            </div>
                                        </li>

                                        <li class="media mb-4">
                                            <a href="#" class="mr-4">
                                                <img src="@/assets/images/faces/4.jpg" class="rounded-circle" width="40" alt="asd" srcset="">
                                            </a>
                                            <div class="ul-task-manager__media">
                                                <a href="">James Alexander</a>
                                                <div class="font-size-sm text-muted">Santa Ana,CA</div>
                                            </div>
                                            <div class="ml-3 align-self-center">
                                                <span class="badge badge-mark "></span>
                                            </div>
                                        </li>

                                        <li class="media ">
                                            <a href="#" class="mr-4">
                                                <img src="@/assets/images/faces/3.jpg" class="rounded-circle" width="40" alt="asd" srcset="">
                                            </a>
                                            <div class="ul-task-manager__media">
                                                <a href="">James Alexander</a>
                                                <div class="font-size-sm text-muted">Santa Ana,CA</div>
                                            </div>
                                            <div class="ml-3 align-self-center">
                                                <span class="badge badge-mark"></span>
                                            </div>
                                        </li>
                                    </ul>
                                </b-card-body>
                            </b-collapse>
                        </b-card>
                    </b-col>-->

                   
                   

                   <!-- completeness-stats -->
                   <!--
                    <b-col md="12">
                        <b-card  
                            b-card-link
                            no-body
                            class="mb-30  o-hidden">
                            <b-card-header 
                                style="cursor:pointer"
                                v-b-toggle.collapse-6>
                                Completeness Stats
                            </b-card-header>
                            <b-collapse 
                                visible 
                                id="collapse-6" 
                                class="mt-2">
                                <b-card-body>
                                    <b-list-group>
                                        <b-list-group-item class="mb-3 border-0">
                                            <div class="d-flex align-items-center  mb-1">Blockers <span class="text-muted ml-auto">50%</span></div>
                                            <b-progress height="2px" :value="value"></b-progress>
                                        </b-list-group-item>
                                        <b-list-group-item class="mb-3 border-0">
                                            <div class="d-flex align-items-center  mb-1">High Priority <span class="text-muted ml-auto">50%</span></div>
                                            <b-progress variant="danger" height="2px" :value="value"></b-progress>
                                        </b-list-group-item>
                                        <b-list-group-item class="mb-3 border-0">
                                            <div class="d-flex align-items-center  mb-1">Normal Priority <span class="text-muted ml-auto">50%</span></div>
                                            <b-progress variant="success" height="2px" :value="value"></b-progress>
                                        </b-list-group-item>
                                        <b-list-group-item class="mb-3 border-0">
                                            <div class="d-flex align-items-center  mb-1">Low Priority <span class="text-muted ml-auto">50%</span></div>
                                            <b-progress variant="warning" height="2px" :value="value"></b-progress>
                                        </b-list-group-item>
                                        
                                    </b-list-group>
                                </b-card-body>  
                            </b-collapse>
                        </b-card>
                    </b-col>
                </b-row>
            </b-col>
        </b-row>-->

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
                  <div style="display: flex; justify-content:space-between; background-color:#fff;" class="p-3 rounded text-center">
                    <h4 class="card-title mb-3">Exclusive datatable plugin</h4>
                    <p>
                      <i class="i-Gear"></i>
                    </p>
                  </div>
                 <!--
                  <div class="card-body">
                    <div>
                        <b-table
                          id="my-table"
                          :items="items"
                          :per-page="perPage"
                          :current-page="currentPage"
                          small
                          
                          
                        >
                        
                          
                          <template #cell(selected)="data" >
                            <b-form-checkbox v-model="data.item.selected"></b-form-checkbox>
                            
                          </template>
                          
                          
                          <template #cell(actions)="data">
                            <b-dropdown variant="secondary" text="Actions" no-caret>
                              <b-dropdown-item @click="editItem(data.items)">Edit</b-dropdown-item>
                              <b-dropdown-item @click="deleteItem(data.items)">Delete</b-dropdown-item>
                            </b-dropdown>
                          </template>
                        </b-table>
                    
                        <b-button @click="deleteSelected" class="bg-primary btn m-3">Delete Selected</b-button>
                        <b-pagination
                          v-model="currentPage"
                          :total-rows="rows"
                          :per-page="perPage"
                          aria-controls="my-table"
                        ></b-pagination>
                    </div>
                    
                  </div>-->

                    <div class="table-responsive">
                        
                    
                        <!-- Table 1 -->
                        <table class="table" v-show="first_table">
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
                                    <td><img :src="person.img" class="img"></td>
                                    <td><img :src="person.img" class="img"></td>
                                    <td> {{person.status}} </td>
                                    <td>
                                        <b-button :variant="getColorVariant(index)" class="m-1">{{ person.items }}</b-button>
                                    </td>
                                    
                                   
                                    <td>{{person.fees1}}
                                        <br> {{ person.fees2 }}
                                    </td>
                                    <td>
                                        <b-dropdown id="dropdown-1" text="Dropdown">
                                            <b-dropdown-item @click="deleteSelected">Delete</b-dropdown-item>
                                            <b-dropdown-item @click="handleItemClick('Item 2')">Add</b-dropdown-item>
                                            
                                        </b-dropdown>
                                    </td>

                                    <!-- Add more columns as needed -->
                                </tr>
                            </tbody>
                        </table>
            
                        <!-- Table 2 -->
                        <table class="table" v-show="second_table">
                            <thead>
                                <tr>
                                    <th scope="col">#</th>
                                    <th scope="col">Recipent </th>
                                    <th scope="col">Merchant </th>
                                    <th scope="col">Status</th>
                                    <th scope="col">Item</th>
                                    <th scope="col">Fees</th>
                                    <th scope="col">Actions</th>
                                    <!-- Add more headers as needed -->
                                </tr>
                            </thead>
                            <tbody>
                                <tr v-for="(person, index) in people2" :key="index">
                                    <td>
                                        <input type="checkbox" v-model="person.selected">
                                      </td>
                                    <td><img :src="person.img" class="img"></td>
                                    <td>{{person.Merchant}}</td>
                                    <td>
                                        <b-button :variant="getColorVariant(index)" class="m-1">{{ person.Status }}</b-button>
                                    </td>
                                    
                                    <td>{{person.items1}}
                                        <br> {{ person.items2 }}
                                    </td>
                                    <td><button class="btn btn-transparent">...</button></td>
                                    <td>
                                        <b-dropdown id="dropdown-1" text="Dropdown">
                                            <b-dropdown-item @click="deleteSelected">Delete</b-dropdown-item>
                                            <b-dropdown-item @click="handleItemClick('Item 2')">Add</b-dropdown-item>
                                            
                                        </b-dropdown>
                                    </td>

                                    <!-- Add more columns as needed -->
                                </tr>
                            </tbody>
                        </table>
            
                        
                    </div>
                    <!-- Pagination Controls -->
                    <div class="pagination m-5">
                        <button @click="prevPage" class="btn btn-secondary">Previous Page</button>
                        <button @click="nextPage" class="btn btn-secondary">Next Page</button>
                    </div>

                    
              </div>
          </div>
        </div>

        

        

        <!-- <div class="wrapper"> -->
            <!--
        <vue-good-table
        :columns="columns"
        :line-numbers="true"
        :search-options="{
        enabled: true,
        placeholder: 'Search this table',
        }"
        :pagination-options="{
        enabled: true,
        mode: 'records',
        }"
        styleClass="tableOne vgt-table"
        :selectOptions="{
        enabled: true,
        selectionInfoClass: 'table-alert__box',
        }"
        :rows="rows"
    >
            <div slot="table-actions" class="mb-3">
                <b-button variant="light" class="btn-rounded">
                    ...
                </b-button>
            </div>

            <template slot="table-row" slot-scope="props">
                <span v-if="props.column.field == 'button'">
                    <a href="">
                        <i class="i-Eraser-2 text-25 text-success mr-2"></i>
                    {{ props.row.button }}</a
                    >
                    <a href="">
                        <i class="i-Close-Window text-25 text-danger"></i>
                    {{ props.row.button }}</a
                    >
                </span>
            </template>
        </vue-good-table>
        -->

    </div>
</template>
<!--
<script>

export default {
    
           metaInfo: {
      // if no subcomponents specify a metaInfo.title, this title will be used
        title: "Task Manager"
    },*/
    /*
    data() {
      return {
        //value: 75,

        // pagination
        /*
        perPage: 3,
        currentPage: 1,
        items: [
          { id: 1, first_name: 'Fred', last_name: 'Flintstone' },
          { id: 2, first_name: 'Wilma', last_name: 'Flintstone' },
          { id: 3, first_name: 'Barney', last_name: 'Rubble' },
          { id: 4, first_name: 'Betty', last_name: 'Rubble' },
          { id: 5, first_name: 'Pebbles', last_name: 'Flintstone' },
          { id: 6, first_name: 'Bamm Bamm', last_name: 'Rubble' },
          { id: 7, first_name: 'The Great', last_name: 'Gazzoo' },
          { id: 8, first_name: 'Rockhead', last_name: 'Slate' },
          { id: 9, first_name: 'Pearl', last_name: 'Slaghoople' }
        ]*/
        /*
        columns: [
        {
          label: "Receipt",
          field: "receipt",
        },
        {
          label: "Span",
          field: "span",
          html: true,
        },
        {
          label: "Created On",
          field: "createdAt",
          type: "date",
          dateInputFormat: "yyyy-mm-dd",
          dateOutputFormat: "MMM Do yy",
        },
        {
          label: "Percent",
          field: "score",
          type: "percentage",
        },
        {
          label: "Button",
          field: "button",
          html: true,
          tdClass: "text-right",
          thClass: "text-right",
        },
        ],
        rows: [
            {
            id: 1,
            receipt: "@/assets/images/mac_book.jpg",
            span: '<span class="badge badge-primary">Primary</span>',
            createdAt: "2019-10-29",
            score: 0.03343,
            },
            {
            id: 2,
            name: "Jane",
            span: '<span class="badge badge-danger">Primary</span>',
            createdAt: "2011-10-31",
            score: 0.03343,
            },
            {
            id: 3,
            name: "Susan",
            span: '<span class="badge badge-warning">Primary</span>',
            createdAt: "2011-10-30",
            score: 0.03343,
            },
            {
            id: 4,
            name: "Chris",
            span: '<span class="badge badge-primary">Primary</span>',
            createdAt: "2011-10-11",
            score: 0.03343,
            },
            {
            id: 5,
            name: "Dan",
            span: '<span class="badge badge-danger">Primary</span>',
            createdAt: "2011-10-21",
            score: 0.03343,
            },
            {
            id: 6,
            name: "John",
            span: '<span class="badge badge-success">success</span>',
            createdAt: "2011-10-31",
            score: 0.03343,
            },
            {
            id: 1,
            name: "John",
            span: '<span class="badge badge-warning">Warning</span>',
            createdAt: "2019-10-29",
            score: 0.03343,
            },
            {
            id: 2,
            name: "Jane",
            span: '<span class="badge badge-info">Info</span>',
            createdAt: "2011-10-31",
            score: 0.03343,
            },
            {
            id: 3,
            name: "Susan",
            span: '<span class="badge badge-dark">Dark</span>',
            createdAt: "2011-10-30",
            score: 0.03343,
            },
            {
            id: 4,
            name: "Chris",
            span: '<span class="badge badge-warning">Warning</span>',
            createdAt: "2011-10-11",
            score: 0.03343,
            },
            {
            id: 5,
            name: "Dan",
            span: '<span class="badge badge-info">Info</span>',
            createdAt: "2011-10-21",
            score: 0.03343,
            },
            {
            id: 6,
            name: "John",
            span: '<span class="badge badge-primary">Primary</span>',
            createdAt: "2011-10-31",
            score: 0.03343,
            },
        ],
        */
      }
    },
    computed: {
        /*
      rows() {
        return this.items.length
      }*/
    },

    methods: {
        addFile() {
        // console.log("hello");
        },
    },
    }

</script>
-->


<script>
export default{
    data(){
        return{
            colorVariants: ['warning', 'primary', 'success', 'info', 'danger'], // Define your color variants
            first_table: true,
            second_table: false,
            perPage: 5,
            currentPage: 1,
            
            people: [
                { status: '11/28/2016', items: 'Waiting', selected: false, img: require("@/assets/images/products/foodkart-image.jpg"), fees1:'UI Lib', fees2:'Angular 2.Vue.js'},
                { status: '11/28/2016', items: 'Waiting', selected: false,img: require("@/assets/images/products/foodkart-image2.jpg"), fees1:'UI Lib', fees2:'Angular 2.Vue.js' },
                { status: '11/28/2016', items: 'Delivered', selected: false, img: require("@/assets/images/products/foodkart-image3.jpg"), fees1:'UI Lib', fees2:'Angular 2.Vue.js' },
                { status: '11/28/2016', items: 'Delivered', selected: false, img: require("@/assets/images/products/foodkart-image4.jpg"), fees1:'UI Lib', fees2:'Angular 2.Vue.js'},
                { status: '11/28/2016', items: 'Processing', selected: false,img: require("@/assets/images/products/foodkart-image.jpg"), fees1:'UI Lib', fees2:'Angular 2.Vue.js' }
                
            ],
            people2: [
                { img: require("@/assets/images/products/foodkart-image.jpg"), Merchant: '11/28/2017', Status: 'Processing', selected: false,  items1:'UI Lib', items2:'Angular 2.Vue.js'},
                { img: require("@/assets/images/products/foodkart-image2.jpg"), Merchant: '11/28/2017', Status: 'Processing', selected: false, items1:'UI Lib', items2:'Angular 2.Vue.js'  },
                { img: require("@/assets/images/products/foodkart-image3.jpg"), Merchant: '11/28/2017', Status: 'Processing', selected: false,  items1:'UI Lib', items2:'Angular 2.Vue.js' },
                { img: require("@/assets/images/products/foodkart-image.jpg"), Merchant: '11/28/2017', Status: 'Processing', selected: false,  items1:'UI Lib', items2:'Angular 2.Vue.js'},
                { img: require("@/assets/images/products/foodkart-image2.jpg"), Merchant: '11/28/2017', Status: 'Processing', selected: false, items1:'UI Lib', items2:'Angular 2.Vue.js' }
                
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