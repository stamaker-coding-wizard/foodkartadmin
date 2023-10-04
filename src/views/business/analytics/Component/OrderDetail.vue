<template>
    <div>
        
        <b-row class="categoryBox">
            <!-- ICON BG -->
            <b-col lg="4" md="8" sm="12" v-for="Order in Orders" :key="Order.orderid" style="cursor:pointer;">
                
              <b-card
                class=" o-hidden mb-30 text-center categoryCard"
              >
                <div class="cateContent">
                    <div class="cateFlex1">
                        <h4>{{ Order.orderid}} </h4>
                        <h5>{{ Order.deliveryDate }}</h5>
                    </div>
                    <div class="cateUrl">
                        <img :src="Order.Url">
                    </div>
                </div>
                <div class="cateContent">
                    
                    <div class="cateFlex2">
                        <h5>{{ Order.arrive }}</h5>
                        <h4>{{ Order.mins }} </h4>
                    </div>
                    <b-button pill variant="success m-1">Details</b-button>
                </div>
              </b-card>
            </b-col>
            
            
            
        </b-row>
    </div>
</template>

<script>
export default {
    name: 'Category',

    data(){
        return{
            Orders: [
                {orderid: "ASDR34R", deliveryDate:"23 march 2023, 08:23pm", Url: require("@/assets/images/products/groceries1.jpg"), arrive:"Estimated Arrival", mins: "20 mins", Content:"NetCafe"},
                {orderid: "ASDR34R", deliveryDate:"23 march 2023, 08:23pm", Url: require("@/assets/images/products/groceries2-removebg-preview.png"), arrive:"Estimated Arrival", mins: "20 mins", Content:"Groceries" },
                {orderid: "ASDR34R", deliveryDate:"23 march 2023, 08:23pm", Url: require("@/assets/images/products/shawama.jpg"), arrive:"Estimated Arrival", Content:"Shawama", mins: "20 mins", },
                
            ]
        }
    }
}
</script>

<style scoped>
.categoryBox{
    background-color: #fff;
    padding: 10px;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}
.categoryCard{
    background-color: aliceblue;
}
.cateContent{
    width: 100%;
    margin-top: 10px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.cateUrl img{
    width: 60px;
    height: 60px;
    border-radius: 50%;

}
.cateFlex1, .cateFlex2{
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
}
.cateFlex1 h4{
    color: #10b981 !important;
}
.cateFlex1 h5{
    color: gray;
    font-size: 17px;
    font-weight: 700;
}
.cateFlex2 h5{
    color: gray;
    font-size: 14px;
    font-weight: 700;
}
.cateFlex2 h4{
    color: #000;
    font-size: 17px;
    font-weight: 800;
}





</style>