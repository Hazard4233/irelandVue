<template>
    <div class="portfolio-page">
        <v-container fluid>
            <v-row>
                <v-col cols="3" sm="4" md="4" lg="4" xl="3">
                    <div class="font-coolvetica" style="font-size: 70pt;color:white;">Portfolio</div>
                </v-col>
                <v-col cols="6" sm="7" md="7" lg="6" xl="6"></v-col>
                <v-col cols="3" sm="1" md="1" lg="2" xl="3" class="menu">
                    <button class="menu-btn" v-if="isshowed_menu_list === 'none'" @click="MenuBtn_Clicked">
                        <i class="fa fa-reorder" style="font-size:24px"></i>
                    </button>
                    <button class="menu-btn" v-if="isshowed_menu_list === 'block'" @click="MenuBtn_Clicked" style="text-align: center;">&#x2573;</button>
                    <div class="sub-menu-list" v-bind:style="{display: isshowed_menu_list}">
                        <div class="sub-menu">
                            <v-btn text small>Home</v-btn>
                        </div>
                        <div class="sub-menu">
                            <v-btn text small color="error">Blog</v-btn>
                        </div>
                        <div class="sub-menu">
                            <v-btn text small>Misc</v-btn>
                        </div>
                        <div class="sub-menu">
                            <v-btn text small color="error">Contact</v-btn>
                        </div>
                    </div>
                </v-col>
            </v-row>
            <div class="portfolio-main">
                <v-row style="direction: ltr;">
                    <v-col cols="12" sm="12" md="4" lg="4" xl="4">
                        <PortfolioItem2 title="Potluck" detail="This project was about learning how to play 
around with  nodejs and connecting an API 
the mealdb api to it. Everytime you reload 
you get a new recipe to try, hence the name 
potluck."/>
                       <PortfolioItem2 title="Potluck" detail="This project was about learning how to play 
around with  nodejs and connecting an API 
the mealdb api to it. Everytime you reload 
you get a new recipe to try, hence the name 
potluck."/>
                        <PortfolioItem2 title="Potluck" detail="This project was about learning how to play 
around with  nodejs and connecting an API 
the mealdb api to it. Everytime you reload 
you get a new recipe to try, hence the name 
potluck."/>
                    </v-col>
                    <v-col cols="12" sm="12" md="4" lg="4" xl="4">
                        <PortfolioItem2 title="Potluck" detail="This project was about learning how to play 
around with  nodejs and connecting an API 
the mealdb api to it. Everytime you reload 
you get a new recipe to try, hence the name 
potluck. This project was about learning how 
to play around with  nodejs and connecting 
an API the mealdb api to it. Everytime you 
reload you get a new recipe to try, hence the 
name potluck."/>
                        
                    </v-col>
                    <v-col cols="12" sm="12" md="4" lg="4" xl="4" style="padding-top: 250px">
                        <PortfolioItem2 title="Potluck" detail="This project was about learning how to play 
around with  nodejs and connecting an API 
the mealdb api to it. Everytime you reload 
you get a new recipe to try, hence the name 
potluck. This project was about learning how 
to play around with  nodejs and connecting 
an API the mealdb api to it. Everytime you"/>
                    </v-col>
                </v-row>
            </div>
        </v-container>
    </div>
</template>
<script>
import PortfolioItem2 from '../components/Portfolio/PortfolioItem2'
export default {
    data() {
        return {
            isshowed_menu_list: "none",
        }
    },
    components: {
        PortfolioItem2
    },
    methods: {
        MenuBtn_Clicked() {
            console.log("isshowed_menu_list=", this.isshowed_menu_list);
            if(this.isshowed_menu_list == "none") this.isshowed_menu_list = "block"
            else this.isshowed_menu_list = "none"
        }
    }
}   
</script>
<style scoped>
.row {
    margin: 0px;
}
.portfolio-page {
    background-color: black;
    height: 100vh;
    padding-left: 50px;
    padding-top: 80px;
}
.center-css {
    display: flex;
    justify-content: center;
    align-items: center;
}
.portfolio-main {
    overflow-x: hidden;
    overflow-y: scroll;
    height: 600px;
    direction: rtl;
    margin-right: 100px;
    padding-left: 20px;
}
.menu .menu-btn {
    background: #f2fe02;
    width: 50px;
    height: 40px;
    border-radius: 5px;
    font-weight: bold;
    font-size: 10pt;
    margin-right: 10px;
    margin-top: -80px;
    float: right;
}
.menu .sub-menu-list {
    display: none;
    float: right;
    width: 120px;
    margin-right: 60px;
    margin-top: -80px;
}
.menu .sub-menu-list .sub-menu button {
    color: white;
    margin-bottom: 15px;
}
.menu .sub-menu {
    text-align: left;
    margin-right: 10px;
}
@media only screen and ( max-width: 900px) {
    .portfolio-page {
        padding-left: 10px;
    }
}
</style>