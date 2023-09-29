<template>
<div class="row mb-2">
        <div class="col-md-6" v-for="(n,i) in travelList" :key="n">
          <div class="row g-0 border rounded overflow-hidden flex-md-row mb-4 shadow-sm h-md-250 position-relative">
            <div class="col p-4 d-flex flex-column position-static">
              <strong class="d-inline-block mb-2 text-primary-emphasis"> {{ i+1 }} </strong>
              <h3 class="mb-0">{{n.name}}</h3>
              <div class="mb-1 text-body-secondary">ราคาต่อโต๊ะ {{n.price}} บาท</div>
              <p class="card-text mb-auto">{{n.text_box}}</p>
              
              <div style="margin-bottom: 30px;">
              <RouterLink :to="{name: `news_${i+1}` , params: {id: n.name}}" class="icon-link gap-1 icon-link-hover stretched-link">
               รายละเอียดเพิ่มเติม
                <svg class="bi"> <use xlink:href="#chevron-right"/></svg>
             </RouterLink>
            </div>     
            </div>
            <div class="col-auto d-none d-lg-block">
              <svg class="bd-placeholder-img" width="200" height="250" xmlns="http://www.w3.org/2000/svg" role="img"  preserveAspectRatio="xMidYMid slice" focusable="false" 
              style="margin: 15px;" >
                <image :xlink:href="n.img" x="0" y="10" width="200" height="200" />
              </svg>
            </div>
          </div>
        </div>
    </div>
</template>

<script setup>

import { RouterLink } from 'vue-router'
import { ref } from 'vue';

const travelList=ref([
   {name: 'The Good View',  price:200, img:"https://www.reviewchiangmai.com/wp-content/uploads/2021/12/01_Goodview.png", quantity: 0 ,
    text_box:'10:00-23:00'
    }, 
  
    {name:'Too Nice Nimman',    price:200, img:"https://www.reviewchiangmai.com/wp-content/uploads/2021/12/02_Too-Nice-Nimman.jpg", quantity: 0 ,
    text_box:'19:00-23:00'
    },
    
    {name:'The PARK Society Bar & Hostel',   price:200, img:"https://www.reviewchiangmai.com/wp-content/uploads/2021/12/03_The-park-society.jpg", quantity: 0 ,
    text_box:'19:00-23:00'
    },
    
    {name:'Lism cafe Chiangmai',     price:200, img:"https://www.reviewchiangmai.com/wp-content/uploads/2021/12/04_Lism-cafe.jpg", quantity: 0 ,
    text_box:'19:00-23:00'
    },
    
    {name:'Porjai Bar Chiangmai',  price:200, img:"https://www.reviewchiangmai.com/wp-content/uploads/2021/12/05_-PORJAI-BAR.jpg", quantity: 0 ,
    text_box:'18:00-23:50'
    },
    
    {name:'บางขวาง Cafe’ Chiangmai',  price:200,  img:"https://www.reviewchiangmai.com/wp-content/uploads/2021/12/06_%E0%B8%9A%E0%B8%B2%E0%B8%87%E0%B8%82%E0%B8%A7%E0%B8%B2%E0%B8%87-%E0%B8%84%E0%B8%B2%E0%B9%80%E0%B8%9F%E0%B9%88.jpg", quantity: 0 ,
    text_box:'17:00-00:00'
    },
])


</script>

<style>
  .row {
    background-color: #f5f5f5; 
  }

  h3 {
    color: #333; 
  }
  .row {
    background-color: #f5f5f5;
    padding: 20px;
    margin-bottom: 20px; 
  }

  h3 {
    color: #333;
    font-size: 24px; 
  }

  .row {
    background-color: #e6c1f3;
    padding: 20px; 
  }

  h3 {
    color: #333;
    font-size: 24px;
  }

  .icon-link {
    text-decoration: none; 
    color: #0084ff;
    transition: color 0.2s;
  }

  .icon-link:hover {
    color: #ff0000; 
  }
  
  .shadow-box {
    box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.2); 
  }



</style>

