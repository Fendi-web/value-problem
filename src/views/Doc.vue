<template>
    <div>
        <Topnav/>
    <div class="topnav">
         <div class="log"></div>
         <div class="menu"></div>
     </div> 
     <div class="content">
         <aside>
             <h2>组建列表</h2>
             <ol>
                 <li>
                     <router-link to="/doc/switch">switch 组件</router-link>
                 </li>
                 <li>
                     <router-link to="/doc/button">Button 组件</router-link>
                 </li>
                 <li>
                     <router-link to="/doc/dialog">Dialog 组件</router-link>
                 </li>
                 <li>
                     <router-link to="/doc/tabs">Tabs 组件</router-link>
                 </li>
             </ol>
         </aside>
         <main>主内容</main>

     </div> 
    </div>
</template>
<script lang="ts">

import Topnav from '../components/Topnav.vue';
import { inject, Ref } from 'Vue';
export default {
    components:{Topnav},
    setup(){
        const menuVisible = inject<Ref<boolean>>('xxx')  
        
    }
    
};
</script>
<style lang="scss" scoped>
aside{
    background:lightblue;
    width: 150px;
    padding:16px;
    position: fixed;
    top:0;
    left:0;
    padding-top: 90px;
    >h2{
        margin-bottom:9px;
    }
    >ol{
        >li{
            padding:9px 0;
        }
    }

}
    
</style>