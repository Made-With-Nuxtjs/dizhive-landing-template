<template>
    <div class="flex justify-center bg-[#f0f2f5]">
        <div
            class="container mx-auto p-3 md:px-48 lg:px-48 xl:px-48  py-8 px-4 sm:px-8 pt-8 md:pt-16 lg:pt-16 xl:pt-16">
            <div class="w-full bg-white rounded-lg border-t-[12px] border-2 border-black shadow-lg">
                <div class="pt-6">
                    <h2 class="text-center text-2xl md:text-4xl lg:text-4xl xl:text-5xl font-bold p-2">অর্ডার করতে
                        নিচের ফর্মটি পূরন করুন
                    </h2>
                    <p
                        class="text-center p-3 text-sm md:text-md lg:text-lg xl:text-lg font-bold italic text-red-600 underline underline-offset-1">
                        ** নগদ, রকেট বা উপায় তে পেমেন্ট করতে আমাদের WhatsApp নাম্বারে যোগাজোগ করুন **
                    </p>

                    <div class="flex flex-col lg:flex-row p-6 gap-8">
                        <!-- Billing Details -->
                        <div class="w-full lg:w-1/2 xl:w-1/2">
                            <h5 class="text-md md:text-md text-gray-700 font-bold mb-4">Billing details</h5>
                            <form>
                                <!-- Name Field -->
                                <div class="mb-4">
                                    <label :class="[
                                        'block text-xs font-bold mb-2 transition-colors duration-300',
                                        labelErrors.name ? 'text-red-500' : 'text-gray-800'
                                    ]" for="name">
                                        নাম <span class="text-red-500">*</span>
                                    </label>
                                    <input v-model="formData.name" @focus="focusField('name')"
                                        @blur="validateField('name')"
                                        :placeholder="focusedField === 'name' ? '' : 'আপনার পূরো নাম লিখুন'"
                                        :class="errors.name || labelErrors.name ? 'border-red-400' : 'border-blue-400'"
                                        class="border-2 rounded-xs py-3 w-full text-gray-800 leading-tight placeholder:text-xs placeholder:text-gray-700 placeholder:px-4 focus:outline-none transition-all duration-700"
                                        id="name" type="text" />
                                    <p v-if="errors.name" class="text-xs text-red-500 mt-1">{{ errors.name }}</p>
                                </div>

                                <!-- Mobile Field -->
                                <div class="mb-4">
                                    <label :class="[
                                        'block text-xs font-bold mb-2 transition-colors duration-300',
                                        labelErrors.mobile ? 'text-red-500' : 'text-gray-800'
                                    ]" for="mobile">
                                        মোবাইল নাম্বার<span class="text-red-500">*</span>
                                    </label>
                                    <input v-model="formData.mobile" @focus="focusField('mobile')"
                                        @blur="validateField('mobile')"
                                        :placeholder="focusedField === 'mobile' ? '' : 'আপনার সচল মোবাইল নাম্বার লিখুন'"
                                        :class="errors.mobile || labelErrors.mobile ? 'border-red-400' : 'border-blue-400'"
                                        class="border-2 rounded-xs py-3 w-full text-gray-800 leading-tight placeholder:text-xs placeholder:text-gray-700 placeholder:px-4 focus:outline-none transition-all duration-300"
                                        id="mobile" type="text" />
                                    <p v-if="errors.mobile" class="text-xs text-red-500 mt-1">{{ errors.mobile }}</p>
                                </div>

                                <!-- Email Field -->
                                <div class="mb-4">
                                    <label :class="[
                                        'block text-xs font-bold mb-2 transition-colors duration-300',
                                        labelErrors.email ? 'text-red-500' : 'text-gray-800'
                                    ]" for="email">
                                        ইমেইল<span class="text-red-500">*</span>
                                    </label>
                                    <input v-model="formData.email" @focus="focusField('email')"
                                        @blur="validateField('email')"
                                        :placeholder="focusedField === 'email' ? '' : 'আপনার জিমেইল (Gmail) এড্রেসটি সঠিকভাবে লিখুন'"
                                        :class="errors.email || labelErrors.email ? 'border-red-400' : 'border-blue-400'"
                                        class="border-2 rounded-xs py-3 w-full text-gray-800 leading-tight placeholder:text-xs placeholder:text-gray-700 placeholder:px-4 focus:outline-none transition-all duration-300"
                                        id="email" type="email" />
                                    <p v-if="errors.email" class="text-xs text-red-500 mt-1">{{ errors.email }}</p>
                                </div>
                            </form>
                        </div>

                        <!-- Order Summary -->
                        <div class="w-full lg:w-1/2 xl:w-1/2 pr-0 md:px-4 lg:px-4 xl:px-4">
                            <h5 class="text-md md:text-md text-gray-700 font-bold mb-4">Your order</h5>
                            <div class="mb-6">
                                <div class="grid grid-cols-1 gap-2 divide-y divide-dashed divide-gray-400">
                                    <div>
                                        <div class="flex justify-between text-sm font-semibold">
                                            <p>Product</p>
                                            <p>Subtotal</p>
                                        </div>
                                    </div>
                                    <div class="pt-2 font-semibold text-gray-600">
                                        <div class="flex justify-between items-center text-sm">
                                            <div class="flex items-center gap-2">
                                                <NuxtImg src="https://placehold.co/32" title="product-image"
                                                    class="w-12" alt="product-image" />
                                                <p>প্রিমিয়াম টিভি এপ</p>
                                            </div>
                                            <p>
                                                <span class="pr-2">&times;&nbsp;1</span> 250.00৳&nbsp;
                                            </p>
                                        </div>
                                    </div>
                                    <div>
                                        <div class="flex justify-between text-sm py-2">
                                            <p>Subtotal</p>
                                            <p>250.00৳</p>
                                        </div>
                                        <div class="flex justify-between text-sm py-1">
                                            <p>bKash Charge</p>
                                            <p>0.00৳</p>
                                        </div>
                                    </div>
                                    <div>
                                        <div class="flex justify-between text-sm font-semibold py-2">
                                            <p>Total</p>
                                            <p>250.00৳</p>
                                        </div>
                                    </div>
                                </div>
                                <div class="bg-gray-100 p-4 mt-4">
                                    <p class="text-sm text-gray-600">বিকাশ অনলাইন পেমেন্ট</p>
                                    <div class="bg-gray-200 p-2 mt-4">
                                        <p class="text-sm text-gray-700">বিকাশের মাধ্যমে পেমেন্ট করুন</p>
                                    </div>
                                </div>
                                <p class="text-xs pt-2 text-gray-600">
                                    Your personal data will be used to process your order, support your experience
                                    throughout this website,
                                    and for other purposes described in our
                                    <a href="#" class="text-red-500">privacy policy</a>.
                                </p>

                                <a href="/success"
                                    class="w-full h-14 flex justify-center items-center gap-3 text-sm font-semibold py-2 rounded-sm bg-[#ec1c24] hover:bg-[#000000] mt-4">
                                    <div>
                                        <svg aria-hidden="true" class="e-font-icon-svg e-fas-lock h-5 w-5 text-white"
                                            fill="currentColor" viewBox="0 0 448 512"
                                            xmlns="http://www.w3.org/2000/svg">
                                            <path
                                                d="M400 224h-24v-72C376 68.92 307.08 0 224 0S72 68.92 72 152v72H48c-26.51 0-48 21.49-48 48v192c0 26.51 21.49 48 48 48h352c26.51 0 48-21.49 48-48V272c0-26.51-21.49-48-48-48zM144 152c0-44.18 35.82-80 80-80s80 35.82 80 80v72H144v-72zm96 200c0 13.25-10.75 24-24 24s-24-10.75-24-24v-48c0-13.25 10.75-24 24-24s24 10.75 24 24v48z">
                                            </path>
                                        </svg>
                                    </div>
                                    <p class="text-lg text-white">অর্ডার করুন 250.00 ৳&nbsp;</p>
                                </a>

                            </div>
                        </div>
                    </div>

                </div>
            </div>
        </div>
    </div>
</template>


<script setup>
import { reactive, ref } from 'vue';

// Form data reactive object
const formData = reactive({
    name: '',
    mobile: '',
    email: '',
});

// Error messages reactive object for field errors
const errors = reactive({
    name: null,
    mobile: null,
    email: null,
});

// Reactive object to handle label color errors
const labelErrors = reactive({
    name: false,
    mobile: false,
    email: false,
});

// Track the focused field for placeholder logic
const focusedField = ref('');

// Function to focus on an input field
const focusField = (field) => {
    focusedField.value = field;
};

// Function to validate each field
const validateField = (field) => {
    const value = formData[field].trim();

    // Reset errors initially
    errors[field] = null;
    labelErrors[field] = false;

    // Check if the field is empty
    if (!value) {
        errors[field] = `${field === 'name' ? 'নাম' : field === 'mobile' ? 'মোবাইল নাম্বার' : 'ইমেইল'} লিখুন`;
    }

    // Perform format validation if the field is not empty
    else {
        if (field === 'name' && !/^[a-zA-Z\s]+$/.test(value)) {
            labelErrors[field] = true;
        } else if (field === 'mobile' && !/^\d{11}$/.test(value)) {
            labelErrors[field] = true;
        } else if (field === 'email' && !/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(value)) {
            labelErrors[field] = true;
        }
    }
};
</script>
