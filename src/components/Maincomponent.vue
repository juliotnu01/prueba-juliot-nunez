<script setup>
import { onMounted, ref } from 'vue';
import { DoughnutChart, BarChart } from 'vue-chart-3';
import { Chart, registerables } from "chart.js";
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Navigation, Pagination, Mousewheel, Keyboard } from 'swiper';
import axios from 'axios'
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';
Chart.register(...registerables);
const testData = {
    labels: ['Paris', 'Nîmes', 'Toulon', 'Perpignan', 'Autre'],
    datasets: [
        {
            data: [30, 40, 60, 70, 5],
            backgroundColor: ['#77CEFF', '#0079AF', '#123E6B', '#97B0C4', '#A5C8ED'],
        },
    ],
};
const modules = [Navigation, Pagination, Mousewheel, Keyboard];
const imagenSlide = ref([]);
const getImgForSlide = async () => {
    try {
        let { data } = await axios('https://picsum.photos/v2/list?page=2&limit=5');
        imagenSlide.value = data.map(item => item.download_url)
    } catch (e) {
        console.log(e)
    }
}
onMounted(() => {
    getImgForSlide()
})
</script>
<template >
        <div>
            <div class="w-[650px] h-[350px] bg-[#272E35] rounded-[17px] p-6 max-[640px]:w-[380px]">
                <div class="flex justify-between px-8 w-full">
                    <span class="font-bold">Best Selling</span>
                    <span class="flex gap-2">
                        This Week
                        <svg fill="#fff" width="20px" height="20px" viewBox="0 0 24 24" class="self-center ">
                            <path
                                d="M17,8H7a1,1,0,0,0-.768,1.641l5,6a1,1,0,0,0,1.536,0l5-6A1,1,0,0,0,17,8Zm-5,5.438L9.135,10h5.73Z" />
                        </svg>
                    </span>
                </div>
                <div class="w-full h-8 bg-[#20262D] rounded-lg flex justify-between px-8 items-center mt-2">
                    <span class=" text-[16px] ">Tuesday</span>
                    <span class=" text-[16px] ">215,523 pcs</span>
                </div>
                <div class="w-full h-4/6 mt-14 flex gap-2 ">
                    <div class=" w-full h-full">
                        <DoughnutChart :chartData="testData" :width="150" :height="150" />
                    </div>
                    <div class=" w-full h-full max-[640px]:hidden">
                        <BarChart :chartData="testData" :width="150" :height="150" />
                    </div>
                </div>
            </div>
            <div class="grid grid-cols-2 gap-4 mt-12 max-[640px]:grid-cols-1 ">
                <div class="w-full h-36 bg-[#2F363D] rounded-[17px] py-4" v-for="n in 4" :key="n">
                    <div class="flex flex-col justify-between px-8 w-full">
                        <div class="flex justify-between -mb-2">
                            <span class="font-bold">456k Pcs</span>
                            <span class="flex gap-2 text-[#B7B7B7] text-[12px]">
                                Daily
                                <svg fill="#B7B7B7" width="20px" height="20px" viewBox="0 0 24 24" class="self-center ">
                                    <path
                                        d="M17,8H7a1,1,0,0,0-.768,1.641l5,6a1,1,0,0,0,1.536,0l5-6A1,1,0,0,0,17,8Zm-5,5.438L9.135,10h5.73Z" />
                                </svg>
                            </span>
                        </div>
                        <div class="">
                            <span class="text-[12px] text-[#ffffff6d]">Ticket Sold</span>
                        </div>
                        <div class="-mt-2">
                            <BarChart :chartData="testData" :width="150" :height="90" />
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div>
            <div class="w-[650px] h-[250px] bg-gradient-to-r from-[#13B497] to-[#05737A] rounded-lg p-6 max-[640px]:hidden">
                <div class="px-8 w-full flex justify-between">
                    <div>
                        <span class="font-bold">Sales Comparison</span>
                        <span class="flex gap-2">
                            Than last day
                        </span>
                    </div>
                    <div>
                        <span class="flex gap-2 text-4xl font-bold ">
                            94%
                        </span>
                    </div>
                </div>
                <div class=" w-full h-full mt-[25px] ">
                    <BarChart :chartData="testData" :width="100" :height="150" />
                </div>
            </div>
            <div class="h-3/5  my-5 w-full  rounded-lg ">
                <swiper :cssMode="true" :navigation="true" :pagination="true" :mousewheel="true" :keyboard="true"
                    :modules="modules" class="h-full w-full rounded-lg bg-white">
                    <swiper-slide v-for="(imgen, i) in imagenSlide" :key="i">
                        <img height="70" :src="imgen" />
                    </swiper-slide>
                </swiper>
            </div>
        </div>
</template>