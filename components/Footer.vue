<template>
    <footer class="flex justify-center bg-[#f0f2f5]">
        <div class="py-16">
            <div class="w-full bg-white rounded-lg border-t-[12px] border border-[#000000]">
                <div class="pt-4">
                    <h2 class="text-center text-4xl font-bold py-4">অর্ডার করতে নিচের ফর্মটি পূরন করুন</h2>
                    <p class="text-center text-md font-bold italic text-red-600 underline underline-offset-1">
                        ** নগদ, রকেট বা উপায় তে পেমেন্ট করতে আমাদের WhatsApp নাম্বারে যোগাযোগ করুন **
                    </p>

                    <div class="flex flex-row justify-between p-6 gap-4">
                        <div class="w-[550px]">
                            <h5 class="text-md text-gray-700 font-bold mb-6">Billing details</h5>
                            <form class="pr-6">
                                <div class="mb-4">
                                    <label class="block text-gray-800 text-xs font-bold mb-2" for="name">
                                        নাম <span class="text-red-500">*</span>
                                    </label>
                                    <input
                                        class="border border-blue-400 rounded py-2 w-full text-gray-800 leading-tight placeholder:text-xs placeholder:text-gray-700 placeholder:px-4"
                                        id="name" type="text" placeholder="আপনার পুরো নাম লিখুন" />
                                </div>
                                <div class="mb-4">
                                    <label class="block text-gray-800 text-xs font-bold mb-2" for="name">
                                        মোবাইল নাম্বার<span class="text-red-500">*</span>
                                    </label>
                                    <input
                                        class="border border-blue-400 rounded py-2 w-full text-gray-800 leading-tight placeholder:text-xs placeholder:text-gray-700 placeholder:px-4"
                                        id="name" type="text" placeholder="আপনার সচল মোবাইল নাম্বার লিখুন" />
                                </div>
                                <div class="mb-4">
                                    <label class="block text-gray-800 text-xs font-bold mb-2" for="name">
                                        ইমেইল<span class="text-red-500">*</span>
                                    </label>
                                    <input
                                        class="border border-blue-400 rounded py-2 w-full text-gray-800 leading-tight placeholder:text-xs placeholder:text-gray-700 placeholder:px-4"
                                        id="name" type="email"
                                        placeholder="আপনার জিমেইল (Gmail) এড্রেসটি সঠিকভাবে লিখুন" />
                                </div>
                            </form>
                        </div>
                        <div class="w-[480px]">
                            <h5 class="text-md text-gray-700 font-bold mb-6">Your order</h5>
                            <div class="mb-6">
                                <div class="grid grid-cols-1 gap-2 divide-y divide-dashed divide-gray-400">
                                    <div>
                                        <div class="flex justify-between text-sm pr-8 font-semibold">
                                            <p>Product</p>
                                            <p>Subtotal</p>
                                        </div>
                                    </div>
                                    <div class="pt-2 font-semibold text-gray-600">
                                        <div class="flex justify-between items-center text-sm pr-8">
                                            <div class="flex items-center gap-2">
                                                <NuxtImg src="https://placehold.co/32" title="company-logo" class="w-16"
                                                    alt="logo-image" />
                                                <p>প্রিমিয়াম টিভি এপ</p>
                                            </div>
                                            <p>
                                                <span class="pr-2">×&nbsp;1</span>
                                                250.00৳
                                            </p>
                                        </div>
                                    </div>
                                    <div>
                                        <div class="flex justify-between pr-8 text-sm py-2">
                                            <p>Subtotal</p>
                                            <p>250.00৳ </p>
                                        </div>
                                        <div class="flex justify-between pr-8 text-sm py-1">
                                            <p>bKash Charge</p>
                                            <p>0.00৳</p>
                                        </div>
                                    </div>
                                    <div>
                                        <div class="flex justify-between text-sm pr-8 font-semibold py-2">
                                            <p>Total</p>
                                            <p>250.00৳ </p>
                                        </div>
                                    </div>
                                </div>
                                <div class="h-24 bg-gray-100">
                                    <p class="text-sm p-2 text-gray-600">বিকাশ অটোমেটিক পেমেন্ট</p>
                                    <div class="mx-6">
                                        <div class="h-10 bg-gray-200 p-4">
                                            <p class="text-sm text-gray-700 pb-4">বিকাশের মাধ্যমে পেমেন্ট করুন</p> 
                                        </div>
                                    </div>
                                </div>
                                <p class="text-xs pt-2 text-gray-600">
                                    Your personal data will be used to process your order, 
                                    support your experience throughout this website, 
                                    and for other purposes described in our <span class="text-red-500"><a href="#">privacy policy</a></span> .
                                </p>

                                <div class="h-10 bg-red-600 p-4 hover:bg-gray-900">
                                            <p class="text-sm text-gray-700 pb-4">অর্ডার করুন</p> 
                                        </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>
