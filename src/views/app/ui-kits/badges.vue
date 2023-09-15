<template>
  <div class="main-content">
    <breadcumb :page="'Business Hours'" :folder="'Business'" :folder2="'Hours'" />
    <!--
    <b-row>
      <b-col md="6">
        <b-card title="Badge Outline" class="mb-30">
          <b-badge pill variant="outline-primary p-2 m-1">Primary</b-badge>
          <b-badge pill variant="outline-secondary p-2 m-1">Secondary</b-badge>
          <b-badge pill variant="outline-success p-2 m-1">Success</b-badge>
          <b-badge pill variant="outline-danger p-2 m-1">Danger</b-badge>
          <b-badge pill variant="outline-warning p-2 m-1">Warning</b-badge>
          <b-badge pill variant="outline-info p-2 m-1">Info</b-badge>
          <b-badge pill variant="outline-dark p-2 m-1">Dark</b-badge>
        </b-card>
      </b-col>
      <b-col md="6">
        <b-card title="Regular Badges" class="mb-30">
          <b-badge href="#" variant="primary  m-2">Primary</b-badge>
          <b-badge href="#" variant="secondary  m-2">Secondary</b-badge>
          <b-badge href="#" variant="success  m-2">Success</b-badge>
          <b-badge href="#" variant="danger  m-2">Danger</b-badge>
          <b-badge href="#" variant="warning  m-2">Warning</b-badge>
          <b-badge href="#" variant="info  m-2">Info</b-badge>
          <b-badge href="#" variant="light  m-2">Light</b-badge>
          <b-badge href="#" variant="dark  m-2">Dark</b-badge>
        </b-card>
      </b-col>
      <b-col md="6">
        <b-card title="Badge Pill" class="mb-30">
          <b-badge pill variant="primary m-2">Primary</b-badge>
          <b-badge pill variant="secondary m-2">Secondary</b-badge>
          <b-badge pill variant="success m-2">Success</b-badge>
          <b-badge pill variant="danger m-2">Danger</b-badge>
          <b-badge pill variant="warning m-2">Warning</b-badge>
          <b-badge pill variant="info m-2">Info</b-badge>
          <b-badge pill variant="light m-2">Light</b-badge>
          <b-badge pill variant="dark m-2">Dark</b-badge>
        </b-card>
      </b-col>
      <b-col md="6">
        <b-card title="Badge Pill with Padding" class="mb-30">
          <b-badge href="#" pill variant="primary p-2 m-1">Primary</b-badge>
          <b-badge href="#" pill variant="secondary p-2 m-1">Secondary</b-badge>
          <b-badge href="#" pill variant="success p-2 m-1">Success</b-badge>
          <b-badge href="#" pill variant="danger p-2 m-1">Danger</b-badge>
          <b-badge href="#" pill variant="warning p-2 m-1">Warning</b-badge>
          <b-badge href="#" pill variant="info p-2 m-1">Info</b-badge>
          <b-badge href="#" pill variant="light p-2 m-1">Light</b-badge>
          <b-badge href="#" pill variant="dark p-2 m-1">Dark</b-badge>
        </b-card>
      </b-col>

      

      
    </b-row>
    <b-row>
      <b-col md="6">
        <b-card title="Sizing & Styles" class="mb-30">
          <ul class="list-group list-group-flush">
            <h6 class="card-subtitle mt-2 mb-2 text-muted">Medium Size</h6>

            <li class="list-group-item pl-0 border-0">
              <b-badge variant="primary badge-round-primary  m-1">A</b-badge>
              <b-badge variant="primary badge-round-success  m-1">D</b-badge>
              <b-badge variant="primary badge-round-secondary  m-1">C</b-badge>
              <b-badge variant="primary badge-round-danger  m-1">E</b-badge>
              <b-badge variant="primary badge-round-warning  m-1">F</b-badge>
              <b-badge variant="primary badge-round-info  m-1">G</b-badge>
              <b-badge variant="primary badge-round-light  m-1">H</b-badge>
            </li>
            <li class="list-group-item pl-0 border-0">
              <b-badge variant="primary badge-square-primary  m-1">A</b-badge>
              <b-badge variant="primary badge-square-secondary  m-1">D</b-badge>
              <b-badge variant="primary badge-square-success  m-1">C</b-badge>
              <b-badge variant="primary badge-square-danger  m-1">E</b-badge>
              <b-badge variant="primary badge-square-warning  m-1">F</b-badge>
              <b-badge variant="primary badge-square-info  m-1">G</b-badge>
              <b-badge variant="primary badge-square-light  m-1">H</b-badge>
              <b-badge variant="primary badge-square-dark  m-1">I</b-badge>
            </li>

            <h6 class="card-subtitle mt-2 mb-2 text-muted">Large Size</h6>

            <li class="list-group-item pl-0 border-0">
              <b-badge variant="primary badge-round-primary lg m-1">A</b-badge>
              <b-badge variant="primary badge-round-secondary lg m-1">B</b-badge>
              <b-badge variant="primary badge-round-success lg m-1">C</b-badge>
              <b-badge variant="primary badge-round-danger lg m-1">D</b-badge>
              <b-badge variant="primary badge-round-warning lg m-1">E</b-badge>
              <b-badge variant="primary badge-round-info lg m-1">F</b-badge>
              <b-badge variant="primary badge-round-light lg m-1">G</b-badge>
              <b-badge variant="primary badge-round-dark lg m-1">H</b-badge>
            </li>

            <li class="list-group-item pl-0 border-0">
              <b-badge variant="primary badge-square-primary lg m-1">A</b-badge>
              <b-badge variant="primary badge-square-secondary lg m-1">B</b-badge>
              <b-badge variant="primary badge-square-success lg m-1">C</b-badge>
              <b-badge variant="primary badge-square-danger lg m-1">D</b-badge>
              <b-badge variant="primary badge-square-warning lg m-1">E</b-badge>
              <b-badge variant="primary badge-square-info lg m-1">F</b-badge>
              <b-badge variant="primary badge-square-light lg m-1">G</b-badge>
              <b-badge variant="primary badge-square-dark lg m-1">H</b-badge>
            </li>

            <h6 class="card-subtitle mt-2 mb-2 text-muted">Extra Large Size</h6>

            <li class="list-group-item pl-0 border-0">
              <b-badge variant="primary badge-round-primary xl m-1">A</b-badge>
              <b-badge variant="primary badge-round-secondary xl m-1">B</b-badge>
              <b-badge variant="primary badge-round-success xl m-1">C</b-badge>
              <b-badge variant="primary badge-round-danger xl m-1">D</b-badge>
              <b-badge variant="primary badge-round-warning xl m-1">E</b-badge>
              <b-badge variant="primary badge-round-info xl m-1">F</b-badge>
              <b-badge variant="primary badge-round-light xl m-1">G</b-badge>
              <b-badge variant="primary badge-round-dark xl m-1">H</b-badge>
            </li>

            <li class="list-group-item pl-0 border-0">
              <b-badge variant="primary badge-square-primary xl m-1">A</b-badge>
              <b-badge variant="primary badge-square-secondary xl m-1">B</b-badge>
              <b-badge variant="primary badge-square-success xl m-1">C</b-badge>
              <b-badge variant="primary badge-square-danger xl m-1">D</b-badge>
              <b-badge variant="primary badge-square-warning xl m-1">E</b-badge>
              <b-badge variant="primary badge-square-info xl m-1">F</b-badge>
              <b-badge variant="primary badge-square-light xl m-1">G</b-badge>
              <b-badge variant="primary badge-square-dark xl m-1">H</b-badge>
            </li>
          </ul>
        </b-card>

        <b-card title="More Styles & Options" class="mb-30">
          <ul class="list-group list-group-flash">
            <h6 class="card-subtitle mt-2 mb-2 text-muted">Wide badges for longer text:</h6>

            <li class="list-group-item pl-0 border-0">
              <b-badge variant="primary badge-primary w-badge m-1">New</b-badge>
              <b-badge variant="primary badge-dark w-badge m-1">Pending</b-badge>
              <b-badge variant="primary badge-primary w-badge m-1">203</b-badge>
              <b-badge variant="primary badge-success w-badge m-1">hot</b-badge>
              <b-badge variant="primary badge-warning w-badge m-1">fixed</b-badge>
              <b-badge variant="primary badge-info w-badge m-1">in process</b-badge>
              <b-badge variant="primary badge-danger w-badge m-1">completed</b-badge>
            </li>

            <h6 class="card-subtitle mt-2 mb-2 text-muted">Rounded badges examples:</h6>
            <li class="list-group-item pl-0 border-0">
              <b-badge variant="primary badge-primary r-badge m-1">New</b-badge>
              <b-badge variant="primary badge-dark r-badge m-1">Pending</b-badge>
              <b-badge variant="primary badge-primary r-badge m-1">203</b-badge>
              <b-badge variant="primary badge-success r-badge m-1">hot</b-badge>
              <b-badge variant="primary badge-warning r-badge m-1">fixed</b-badge>
              <b-badge variant="primary badge-info r-badge m-1">in process</b-badge>
              <b-badge variant="primary badge-danger r-badge m-1">completed</b-badge>
            </li>
          </ul>
        </b-card>
      </b-col>-->
      <!--
      <b-col md="6">
        
        <b-card title="Unified Styles" class="mb-30">
          <ul class="list-group list-group-flash">
            <h6 class="card-subtitle mt-2 mb-2 text-muted">Circle and Square Unified Styles</h6>

            <li class="list-group-item pl-0 border-0">
              <b-badge variant="primary badge-round  badge-round-opacity-primary  m-1">A</b-badge>
              <b-badge variant="primary badge-round  badge-round-opacity-secondary  m-1">B</b-badge>
              <b-badge variant="primary badge-round  badge-round-opacity-success  m-1">C</b-badge>
              <b-badge variant="primary badge-round  badge-round-opacity-danger  m-1">D</b-badge>
              <b-badge variant="primary badge-round  badge-round-opacity-warning  m-1">E</b-badge>
              <b-badge variant="primary badge-round  badge-round-opacity-info  m-1">F</b-badge>
              <b-badge variant="primary badge-round  badge-round-opacity-dark  m-1">G</b-badge>
            </li>

            <li class="list-group-item pl-0 border-0">
              <b-badge variant="primary badge-square  badge-square-opacity-primary  m-1">A</b-badge>
              <b-badge variant="primary badge-square  badge-square-opacity-secondary  m-1">B</b-badge>
              <b-badge variant="primary badge-square  badge-square-opacity-success  m-1">C</b-badge>
              <b-badge variant="primary badge-square  badge-square-opacity-danger  m-1">D</b-badge>
              <b-badge variant="primary badge-square  badge-square-opacity-warning  m-1">E</b-badge>
              <b-badge variant="primary badge-square  badge-square-opacity-info  m-1">F</b-badge>
              <b-badge variant="primary badge-square  badge-square-opacity-dark  m-1">G</b-badge>
            </li>
          </ul>
        </b-card>

        <b-card class="mb-30" title="Basic Examples">
          <ul class="list-group list-group-flash">
            <h6 class="card-subtitle mb-2 text-muted">Circle and Square Unified Styles:</h6>

            <li class="list-group-item pl-0 border-0">
              <b-badge variant="badge  badge-round-primary sm m-1">A</b-badge>
              <b-badge variant="badge  badge-round-secondary sm m-1">C</b-badge>
              <b-badge variant="badge  badge-round-success sm  m-1">D</b-badge>
              <b-badge variant="badge  badge-round-success pill  m-1">HOT</b-badge>
              <b-badge variant="badge  badge-round-primary pill m-1">NEW</b-badge>
              <b-badge variant="badge  badge-round-danger sm m-1">E</b-badge>
              <b-badge variant="badge  badge-round-warning sm m-1">F</b-badge>
              <b-badge variant="badge  badge-round-info sm m-1">G</b-badge>
              <b-badge variant="badge  badge-round-light sm m-1">H</b-badge>
              <b-badge variant="badge  badge-round-dark sm m-1">I</b-badge>
            </li>
            <ul class="list-group list-group-flash">
              <h6 class="card-subtitle mt-2 mb-2 text-muted">Dot Styles Examples:</h6>

              <li class="list-group-item pl-0 border-0">
                <span class="badge-dot-primary m-1"></span>
                <span class="badge-dot-secondary m-1"></span>
                <span class="badge-dot-success m-1"></span>
                <span class="badge-dot-danger m-1"></span>
                <span class="badge-dot-warning m-1"></span>
                <span class="badge-dot-info m-1"></span>
                <span class="badge-dot-light m-1"></span>
                <span class="badge-dot-dark m-1"></span>
              </li>

              <li class="list-group-item pl-0 border-0">
                Pending
                <span class="badge-dot-primary"></span> Caption
                <span class="badge-dot-secondary"></span> Heading
                <span class="badge-dot-success"></span> Status
                <span class="badge-dot-danger"></span>
              </li>
            </ul>
          </ul>
        </b-card>

        <b-card title="Outline Badges" class="mb-30">
          <ul class="list-group list-group-flash">
            <h6 class="card-subtitle mt-2 mb-2 text-muted">Basic state color badges:</h6>

            <li class="list-group-item pl-0 border-0">
              <b-badge variant="badge outline-round-primary sm m-1">A</b-badge>
              <b-badge variant="badge outline-round-secondary sm m-1">B</b-badge>
              <b-badge variant="badge outline-round-success sm m-1">D</b-badge>
              <b-badge variant="badge outline-round-danger sm m-1">E</b-badge>
              <b-badge variant="badge outline-round-warning sm m-1">F</b-badge>
              <b-badge variant="badge outline-round-info sm m-1">G</b-badge>
              <b-badge variant="badge outline-round-light sm m-1">H</b-badge>
              <b-badge variant="badge outline-round-dark sm m-1">I</b-badge>
            </li>
          </ul>
        </b-card>

        <b-card title="Badge link" class="mb-30">
          <b-badge href="#" variant="primary  m-2">Primary</b-badge>
          <b-badge href="#" variant="secondary  m-2">Secondary</b-badge>
          <b-badge href="#" variant="success  m-2">Success</b-badge>
          <b-badge href="#" variant="danger  m-2">Danger</b-badge>
          <b-badge href="#" variant="warning  m-2">Warning</b-badge>
          <b-badge href="#" variant="info  m-2">Info</b-badge>
          <b-badge href="#" variant="light  m-2">Light</b-badge>
          <b-badge href="#" variant="dark  m-2">Dark</b-badge>
        </b-card>
      </b-col>

      
    </b-row>-->
    <div class="row">
      <div class="col-md-12 mb-3">
        <div class="card text-left">
            <div style="display: flex; justify-content:space-between; background-color:#f1eaea;" class="p-3 rounded text-center">
              <h4 class="card-title mb-3">Opening Days/Time </h4>
              <p>
                Hello
              </p>
            </div>
            <div class="card-body">
                <div class="table-responsive">
                    <table class="table">
                        <thead style="text-align:center;">
                            <tr>
                              <th scope="col">#</th>
                              <th scope="col">Days</th>
                              <th scope="col">Opening Date</th>
                              <th scope="col">Closing Date</th>
                              <th scope="col">Status</th>
                              <th scope="col">Action</th>
                            </tr>
                        </thead>
                        <tbody style="text-align:center;">
                            <tr>
                              <th scope="row">1</th>
                              <td>Monday</td>
                              <td>9:00 am</td>
                              <td>5:00 pm</td>
                              <td><span class="badge badge-success">Open</span></td>
                              <td><a class="text-success mr-2" href="#"><i class="nav-icon i-Pen-2 font-weight-bold"></i></a><a class="text-danger mr-2" href="#"><i class="nav-icon i-Close-Window font-weight-bold"></i></a></td>
                            </tr>
                            <tr>
                              <th scope="row">2</th>
                              <td>Tuesday</td>
                              <td>9:00 am</td>
                              <td>5:00 pm</td>
                              <td><span class="badge badge-success">Open</span></td>
                              <td><a class="text-success mr-2" href="#"><i class="nav-icon i-Pen-2 font-weight-bold"></i></a><a class="text-danger mr-2" href="#"><i class="nav-icon i-Close-Window font-weight-bold"></i></a></td>
                            </tr>
                            <tr>
                              <th scope="row">3</th>
                              <td>Wednesday</td>
                              <td>9:00 am</td>
                              <td>5:00 pm</td>
                              <td><span class="badge badge-success">Open</span></td>
                              <td><a class="text-success mr-2" href="#"><i class="nav-icon i-Pen-2 font-weight-bold"></i></a><a class="text-danger mr-2" href="#"><i class="nav-icon i-Close-Window font-weight-bold"></i></a></td>
                            </tr>
                            <tr>
                              <th scope="row">4</th>
                              <td>Thursday</td>
                              <td>9:00 am</td>
                              <td>5:00 pm</td>
                              <td><span class="badge badge-success">Open</span></td>
                              <td><a class="text-success mr-2" href="#"><i class="nav-icon i-Pen-2 font-weight-bold"></i></a><a class="text-danger mr-2" href="#"><i class="nav-icon i-Close-Window font-weight-bold"></i></a></td>
                            </tr>
                            <tr>
                              <th scope="row">5</th>
                              <td>Friday</td>
                              <td>9:00 am</td>
                              <td>5:00 pm</td>
                              <td><span class="badge badge-danger">Closed</span></td>
                              <td><a class="text-success mr-2" href="#"><i class="nav-icon i-Pen-2 font-weight-bold"></i></a><a class="text-danger mr-2" href="#"><i class="nav-icon i-Close-Window font-weight-bold"></i></a></td>
                            </tr>
                            <tr>
                              <th scope="row">6</th>
                              <td>Saturday</td>
                              <td>9:00 am</td>
                              <td>5:00 pm</td>
                              <td><span class="badge badge-danger">Closed</span></td>
                              <td><a class="text-success mr-2" href="#"><i class="nav-icon i-Pen-2 font-weight-bold"></i></a><a class="text-danger mr-2" href="#"><i class="nav-icon i-Close-Window font-weight-bold"></i></a></td>
                            </tr>
                            <tr>
                              <th scope="row">7</th>
                              <td>Sunday</td>
                              <td>9:00 am</td>
                              <td>5:00 pm</td>
                              <td><span class="badge badge-danger">Closed</span></td>
                              <td><a class="text-success mr-2" href="#"><i class="nav-icon i-Pen-2 font-weight-bold"></i></a><a class="text-danger mr-2" href="#"><i class="nav-icon i-Close-Window font-weight-bold"></i></a></td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>
        </div>
    </div>
    </div>
  </div>
</template>
<script>
export default {
  metaInfo: {
    // if no subcomponents specify a metaInfo.title, this title will be used
    title: "Badges"
  }
};
</script>

