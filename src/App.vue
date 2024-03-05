<script setup>
import { HeatMapComponent as EjsHeatmap, Tooltip } from "@syncfusion/ej2-vue-heatmap";
import { provide } from 'vue';
const heatmap = [Tooltip];
provide('heatmap', heatmap);
const heatmapData = [
        [73, 39, 26, 39, 94, 0],
        [93, 51, 53, 38, 26, 68],
        [99, 28, 22, 4, 66, 34],
        [14, 26, 97, 20, 69, 3],
        [7, 17, 47, 47, 88, 6],
        [41, 55, 73, 23, 3, 79],
        [56, 69, 21, 34, 3, 33],
        [45, 7, 68, 81, 95, 79],
        [60, 77, 74, 68, 88, 51],
        [25, 25, 23, 12, 78, 14],
        [25, 56, 55, 58, 12, 82],
        [74, 33, 88, 23, 86, 59]
    ];
const xAxis = { labels : ['Nancy', 'Andrew','Janet', 'Ian Bell', 'Steven', 'Daniel', 'Robert', 'Laura', 'Anne', 'Paul', 'Karin', 'Mario']}
const yAxis = { labels : ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday']}
const titleSettings = {
    text : 'Sales Revenue per Employee(in 1000 US$)'
}
const cellSettings ={
    tileType : "Bubble",
    bubbleType : "SizeAndColor",
    isInversedBubbleSize : true
}
</script>
<template>
 <ejs-heatmap :dataSource="heatmapData" :titleSettings="titleSettings" :xAxis="xAxis" :yAxis="yAxis"
              height="350px" width="750px" :cellSettings="cellSettings"></ejs-heatmap>
</template>

<style scoped>

</style>
