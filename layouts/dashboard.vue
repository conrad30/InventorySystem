

 <template> 
    <div class="flex flex-col h-screen relative w-screen">
        <naviWrapper class="absolute top-0 z-30 w-screen"/>
    <div class="flex-1">
        <div class="flex">
    <menuWrapper class="z-20"/>
    <nuxt class="pt-20 bg-gray-200 w-full h-screen pb-5 px-5 overflow-y-auto" />
    </div>
        </div>
    </div>
    

</template>

         
<script>
    import NaviWrapper from '~/components/navi/Wrapper.vue';
    import MenuWrapper from '~/components/menu/Wrapper.vue'; 
    import MenuLink from "~/components/Items/MenuLink.vue";
    import MenuLinkList from "~/components/Items/MenuLinkList.vue";


    export default {
    name:"dashboard",
    components: {
    NaviWrapper,
    MenuWrapper,
    MenuLink,
    MenuLinkList
  
        }

    }

    </script>

    