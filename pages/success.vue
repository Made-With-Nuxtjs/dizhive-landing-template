<script setup lang="ts">
useSeoMeta({
    title: 'Order Success-DizHive E-book',
})
</script>

<template>
    <section class="container mx-auto p-3 md:px-48 lg:px-48 xl:px-48">
        <div class="flex justify-center py-4 md:p-16 lg:p-16 xl:p-16">
            <div class="w-full  md:w-[560px] lg:w-[560px] xl:w-[560px]">
                <div class="px-2 flex flex-col items-center gap-2 py-6 shadow-md border-4 xl:border-4 border-[#73b243]">
                    <h3 class="text-xl text-center font-bold">আপনার অর্ডার টি সফল হয়েছে !</h3>
                    <div class="flex justify-center items-center py-6">
                        <div>
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                                    stroke-width="1.5" stroke="currentColor" class="w-6 h-6 text-green-500 mr-2">
                                    <path stroke-linecap="round" stroke-linejoin="round" d="M4.5 12.75l6 6 9-13.5" />
                                </svg>
                        </div>
                        <div>
                            <h3 class="text-2xl text-center font-bold">Successfully Ordered </h3>
                        </div>
                    </div>
                    <a href="/"
                        class="p-3 font-serif text-xl cursor-pointer text-white font-bold rounded-sm transition duration-150 ease-in-out bg-[#73b243] hover:-translate-y-1 hover:scale-110 hover:bg-[#050505]">
                        More Order
                    </a>
                </div>
            </div>

        </div>
    </section>
</template>
