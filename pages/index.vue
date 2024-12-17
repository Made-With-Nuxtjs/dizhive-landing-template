<script setup lang="ts">
useSeoMeta({
    title: 'Checkout (Woo)-DizHive E-book',
})

const isLoaded = ref(false)
const isPlaying = ref(false)
const video = ref()
async function play() {
    await video.value.player.playVideo()
}
function stateChange(event: { data: number; }) {
    isPlaying.value = event.data === 1
}

</script>
<template>
    <main>
        <!-- Hero Section -->
        <section class="container mx-auto p-3 md:px-48 lg:px-48 xl:px-48">
            <div class="flex justify-center items-center p-4 h-48 md:h-32 lg:h-32 xl:h-32">
                <h3 class="text-4xl md:text-5xl lg:text-5xl xl:text-5xl font-bold text-center font-bang px-8">টিভি দেখতে
                    মাসিক বিল দিতে দিতে ক্লান্ত ?
                </h3>
            </div>
        </section>

        <!-- Video Section -->
        <section class="container mx-auto p-3 md:px-48 lg:px-48 xl:px-48">
            <div class="my-5">
                <div class="bg-[#73b243] py-3 flex justify-center items-center h-16 lg:h-12 xl:h-12">
                    <h3
                        class="text-xl md:text-2xl lg:text-2xl xl:text-2xl font-bold px-2 text-white text-center font-bang">
                        তাহলে একবার পেমেন্টেই টিভি দেখুন নিশ্চিন্তে</h3>
                </div>
            </div>
            <ScriptYouTubePlayer ref="video" video-id="d_IFKP1Ofq0" style="width:100%" @ready="isLoaded = true"
                @state-change="stateChange">
                <template #awaitingLoad>
                    <div
                        class="absolute left-1/2 top-1/2 transform -translate-x-1/2 -translate-y-1/2 h-[48px] w-[68px]">
                        <svg height="100%" version="1.1" viewBox="0 0 68 48" width="100%">
                            <path
                                d="M66.52,7.74c-0.78-2.93-2.49-5.41-5.42-6.19C55.79,.13,34,0,34,0S12.21,.13,6.9,1.55 C3.97,2.33,2.27,4.81,1.48,7.74C0.06,13.05,0,24,0,24s0.06,10.95,1.48,16.26c0.78,2.93,2.49,5.41,5.42,6.19 C12.21,47.87,34,48,34,48s21.79-0.13,27.1-1.55c2.93-0.78,4.64-3.26,5.42-6.19C67.94,34.95,68,24,68,24S67.94,13.05,66.52,7.74z"
                                fill="#f00" />
                            <path d="M 45,24 27,14 27,34" fill="#fff" />
                        </svg>
                    </div>
                </template>
            </ScriptYouTubePlayer>
        </section>

        <!-- Features Section -->
        <section class="container mx-auto p-3 md:px-48 lg:px-48 xl:px-48">
            <div class="bg-[#141413] mb-5 flex justify-center items-center h-20 lg:h-14 xl:h-14 px-4">
                <h3 class="text-2xl font-bold font-bang text-white text-center">এই এন্ড্রোয়েড 'নাম' এর
                    ফিচারসমূহঃ</h3>
            </div>
            <div>
                <ul class="list-none ">
                    <li class="flex items-center border border-green-500 p-1">
                        <Icon class="h-8 w-8" name="material-symbols-light:check" style="color: green; padding: 10px;" />
                        <span class="font-bang font-semibold text-lg md:text-2xl lg:text-2xl xl:text-2xl">খেলা দেখার
                            প্রায় সকল চ্যানেল আছে</span>
                    </li>
                    <li class="flex items-center border-x border-b border-green-500 p-1">
                        <Icon class="h-8 w-8" name="material-symbols-light:check" style="color: green; padding: 10px;" />
                        <span class="font-bang font-semibold text-lg md:text-2xl lg:text-2xl xl:text-2xl">বাংলাদেশি
                            প্রায় সকল চ্যানেল আছে</span>
                    </li>
                    <li class="flex items-center border-x border-b border-green-500 p-1">
                        <Icon class="h-8 w-8" name="material-symbols-light:check" style="color: green; padding: 10px;" />
                        <span class="font-bang font-semibold text-lg md:text-2xl lg:text-2xl xl:text-2xl">বাংলাদেশি
                            প্রায় সকল নিউজ চ্যানেল আছে</span>
                    </li>
                    <li class="flex items-center border-x border-b border-green-500 p-1">
                        <Icon class="h-8 w-8" name="material-symbols-light:check" style="color: green; padding: 10px;" />

                        <span class="font-bang font-semibold text-lg md:text-2xl lg:text-2xl xl:text-2xl">ইন্ডিয়ান
                            সিরিয়াল দেখার সকল চ্যানেল আছে</span>
                    </li>
                    <li class="flex items-center border-x border-b border-green-500 p-1">
                        <Icon class="h-8 w-8" name="material-symbols-light:check" style="color: green; padding: 10px;" />
                        <span class="font-bang font-semibold text-lg md:text-2xl lg:text-2xl xl:text-2xl">বাচ্চাদের
                            কার্টুন দেখার সকল চ্যানেল আছে</span>
                    </li>
                    <li class="flex items-center border-x border-b border-green-500 p-1">
                        <Icon class="h-8 w-8" name="material-symbols-light:check" style="color: green; padding: 10px;" />
                        <span class="font-bang font-semibold text-lg md:text-2xl lg:text-2xl xl:text-2xl">এবং আরো অনেক
                            কিছু . . . . .</span>
                    </li>
                </ul>
            </div>
        </section>

        <!-- Objective && Support Section -->
        <section class="container mx-auto p-3 md:px-48 lg:px-48 xl:px-48 font-bang">
            <div
                class="flex flex-col gap-8 md:gap-16 lg:gap-16 justify-center items-center py-8 md:py-12 lg:py-12 xl:py-12">
                <div class="md:w-[560px] lg:w-[560px] xl:w-[560px]">
                    <div
                        class="px-2 rounded-lg shadow-md border-4  md:border-2 lg:border-2 xl:border-2 border-[#73b243]">
                        <h1
                            class="text-[#73b243] text-xl md:text-4xl lg:text-4xl xl:text-4xl font-bold m-4 text-center py-2 md:py-6 lg:py-6 xl:py-6">
                            এই 'নাম' এর বিশেষ বৈশিষ্ট্যঃ
                        </h1>
                        <hr class="border-gray-700 mx-1">
                        <ul class="list-none space-y-2 my-4 font-semibold">
                            <li class="flex items-center text-lg xl:text-2xl">
                                <Icon class="h-8 w-8" name="material-symbols-light:check" style="color: green; padding: 10px;" />
                                <p>সচরাচর কোনো বাফারিং হবে না।</p>
                            </li>
                            <li class="flex items-center text-lg xl:text-2xl">
                                <div>
                                    <Icon class="h-8 w-8" name="material-symbols-light:check" style="color: green; padding: 10px;" />
                                </div>
                                <p>মোবাইল নেটের স্পিড থাকলেও এই এপ্ল টি চলবে।</p>
                            </li>
                            <li class="flex items-center text-lg xl:text-2xl">
                                <div>
                                    <Icon class="h-8 w-8" name="material-symbols-light:check" style="color: green; padding: 10px;" />
                                </div>
                                <p>যেকোনো সময় এপ্লটি আপডেট দিতে পারবেন ফ্রি তে!</p>
                            </li>
                        </ul>
                        <div class="flex justify-center items-center py-6">
                            <div>
                                <Icon class="h-8 w-8" name="material-symbols-light:close" style="color: red;" />
                            </div>
                            <div class="flex justify-center font-semibold pb-4">
                                <div class="w-full">
                                    <h3 class="text-center text-lg xl:text-2xl">এই এপটি শুধুমাত্র এন্ড্রোয়েড অপারেটিং
                                        সিস্টেম
                                        ব্যবহারকারীদের জন্যই তৈরি
                                        হয়েছে।
                                        তাই অন্য কোনো অপারেটিং সিস্টেমের ডিভাইসে এটি চলবে না।
                                    </h3>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="md:w-[560px] lg:w-[560px] xl:w-[560px]">
                    <div
                        class="px-2 flex flex-col items-center gap-2 py-6 border-4  md:border-8 lg:border-8 xl:border-8 border-[#73b243]">
                        <h3 class="text-2xl text-center font-bold font-bang">যেকোনো সমস্যায় সাপোর্ট পেতে যোগাযোগ করুন
                        </h3>
                        <h3 class="text-4xl text-center font-bold pb-4">WhatsApp</h3>
                        <div
                            class="p-4 flex justify-center items-center gap-3 text-2xl cursor-pointer rounded-md transition duration-150 ease-in-out bg-[#73b243] hover:-translate-y-1 hover:scale-110 hover:bg-[#050505]">
                            <div>
                                <svg aria-hidden="true"
                                    class="e-font-icon-svg e-fas-phone-alt h-6 w-6 fill-current text-white hover:fill-white transition duration-300"
                                    viewBox="0 0 512 512" xmlns="http://www.w3.org/2000/svg">
                                    <path
                                        d="M497.39 361.8l-112-48a24 24 0 0 0-28 6.9l-49.6 60.6A370.66 370.66 0 0 1 130.6 204.11l60.6-49.6a23.94 23.94 0 0 0 6.9-28l-48-112A24.16 24.16 0 0 0 122.6.61l-104 24A24 24 0 0 0 0 48c0 256.5 207.9 464 464 464a24 24 0 0 0 23.4-18.6l24-104a24.29 24.29 0 0 0-14.01-27.6z">
                                    </path>
                                </svg>
                            </div>
                            <p class="font-custom text-white font-semibold ">01500-000 000</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- order Section -->
        <section>
            <OrderForm />
        </section>
    </main>


</template>
