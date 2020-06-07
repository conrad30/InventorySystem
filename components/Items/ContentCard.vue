<template>
<!-- 
<template>
<div class="flex flex-col">
<contentCard class="mt-2 mb-4">
<template v-slot:title>
SALES STATISTICS
</template>
<template v-slot:content>
<div class="w-full overflow-hidden p-2">
<barChart :chartdata="
revenueMonthly.barChartData"
:options="revenueMonthly.barChartOptions" :height="120"></barChart>
</div>
</template>
</contentCard>
</div>
 -->

<div class="py-5 bg-white rounded-sm shadow-xl">
        <div class="px-5 py-2 flex-col">
            <div class="text-lg font-thin font-sans tracking-wide">
                <slot name="title"></slot>
            </div>
            <div>
                <slot name="content"></slot>
            </div>
        </div>
    </div>

</template>
