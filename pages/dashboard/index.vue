<template>
        <div class="flex 
            flex-col
            w-56
            transition-all
            duration-500
            ease-in-out
            bg-gray-800
            h-screen
            shadow-2xl
            pt-16
               ">
            
        <menuLink
        :url="'/dashboard'"
            :class= "{
                'text-gray-500':!$route.path.includes('/dashboard'),
                'text-white':$route.path.includes('/dashboard'),
                'hover:bg-gray-600':true,
                'hover:text-white':true
                        }">

        <template v-slot:icon-word>
            <div class="flex items-centerr justify-start overflow-x-hidden">
                <i class="fas fa-home ml-6 mr-4"></i>
                    <label class="flex-shrink-0 ml-2 text-sm font-sans tracking-wide cursor-pointer">Dashboard</label>
                    </div>

                    
                    </template>
                    </menuLink>
                    </div>
                    </template>
                       
<contentCard class="mt-2 mb-4">
<template v-slot:title>
SALES STATISTICS
</template>
<template v-slot:content>
<div class="w-full overflow-hidden p-2">
<barChart :chartData="
revenueMonthly.barChartData"
:options="revenueMonthly.barChartOptions" :height="120"></barChart>
</div>
    </template>
            </contentCard>
        </div>
        </div>
</template>
            



<script>
import ContentCard from "~/components/Items/ContentCard.vue";
import BarChart from '~/components/charts/BarChart';
import LineChart from '~/components/charts/LineChart';
import MenuLink from "~/components/Items/MenuLink.vue";
import MenuLinkList from "~/components/items/MenuLinkList.vue";





const chartColors = {
red: 'rgb(255, 99, 132)',
orange: 'rgb(255, 159, 64)',
yellow: 'rgb(255, 205, 86)',
green: 'rgb(75, 192, 192)',
blue: 'rgb(54, 162, 235)',
purple: 'rgb(153, 102, 255)',
grey: 'rgb(201, 203, 207)'
};


export default {

    components:{
        MenuLink,
        MenuLinkList
    },

transition:{
name:"inventory",
mode:"out-in",
duration: { enter: 1000, leave: 500 },
enterActiveClass: "animated fadeIn",
leaveActiveClass: "animated fadeOut"
},
layout: "dashboard",
components:{
ContentCard,
BarChart,
LineChart
},
data(){
return {
revenueMonthly: {
barChartData: {
labels: ['Jan', 'Feb', 'Mar', 'Apr', 'May'],
datasets: [
{
label: 'Income',

backgroundColor: [
chartColors.green,
chartColors.green,
chartColors.green,
chartColors.green,
chartColors.green],
data: [5, 3, 4, 6, 4]
}
],
},
barChartOptions: {
responsive: true,
legend: {
display: false,
},
title: {
display: true,
text: 'Monthly Income'
},
scales: {
yAxes: [
{
ticks: {
beginAtZero: true,
suggestedMax: 10
}
}
]
}
},
}
}
},
}



</script>
