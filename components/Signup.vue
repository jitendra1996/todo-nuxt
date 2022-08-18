<template>
  <div class="md:mt-0 md:col-span-2">
    <form
      action="#"
      method="POST"
      class="m-auto w-4/6 mt-5"
      @submit.prevent="signupFormHandler"
    >
      <div class="shadow sm:rounded-md sm:overflow-hidden mb-5">
        <div class="px-4 py-5 bg-white sm:p-6">
          <div class="grid grid-cols-6 gap-6">
            <div class="col-span-6 sm:col-span-3">
              <label
                for="first-name"
                class="block text-sm font-medium text-gray-700"
                >First name</label
              >
              <input
                type="text"
                name="first-name"
                id="first-name"
                autocomplete="given-name"
                v-model="firstName"
                class="mt-1 focus:ring-indigo-500 focus:border-indigo-500 block w-full shadow-sm sm:text-sm border-gray-300 rounded-md p-1"
              />
            </div>

            <div class="col-span-6 sm:col-span-3">
              <label
                for="last-name"
                class="block text-sm font-medium text-gray-700"
                >Last name</label
              >
              <input
                type="text"
                name="last-name"
                id="last-name"
                v-model="lastName"
                autocomplete="family-name"
                class="mt-1 focus:ring-indigo-500 focus:border-indigo-500 block w-full shadow-sm sm:text-sm border-gray-300 rounded-md p-1"
              />
            </div>

            <div class="col-span-6 sm:col-span-4">
              <label
                for="email-address"
                class="block text-sm font-medium text-gray-700"
                >Email address</label
              >
              <input
                type="email"
                name="email-address"
                id="email-address"
                v-model="email"
                autocomplete="email"
                class="mt-1 focus:ring-indigo-500 focus:border-indigo-500 block w-full shadow-sm sm:text-sm border-gray-300 rounded-md p-1"
              />
            </div>

            <div class="col-span-6 sm:col-span-4">
              <label
                for="password"
                class="block text-sm font-medium text-gray-700"
                >Password</label
              >
              <input
                type="password"
                name="password"
                v-model="password"
                id="password"
                class="mt-1 focus:ring-indigo-500 focus:border-indigo-500 block w-full shadow-sm sm:text-sm border-gray-300 rounded-md p-1"
              />
            </div>

            <div class="col-span-6 sm:col-span-4">
              <label
                for="confirm-password"
                class="block text-sm font-medium text-gray-700"
                >Confirm Password</label
              >
              <input
                type="password"
                name="confirm-password"
                id="confirm-password"
                v-model="confirmPassword"
                class="mt-1 focus:ring-indigo-500 focus:border-indigo-500 block w-full shadow-sm sm:text-sm border-gray-300 rounded-md p-1"
              />
            </div>

            <div class="col-span-6 sm:col-span-3">
              <label
                for="country"
                class="block text-sm font-medium text-gray-700"
                >Country</label
              >
              <select
                id="country"
                name="country"
                autocomplete="country-name"
                v-model="country"
                class="mt-1 block w-full py-2 px-3 border border-gray-300 bg-white rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm p-1"
              >
                <option value="India">India</option>
                <option value="United State">United States</option>
                <option value="Canada">Canada</option>
                <option value="Mexico">Mexico</option>
              </select>
            </div>

            <div class="col-span-6">
              <label
                for="street-address"
                class="block text-sm font-medium text-gray-700"
                >Street address</label
              >
              <input
                type="text"
                name="street-address"
                id="street-address"
                autocomplete="street-address"
                v-model="streetAddress"
                class="mt-1 focus:ring-indigo-500 focus:border-indigo-500 block w-full shadow-sm sm:text-sm border-gray-300 rounded-md p-1"
              />
            </div>

            <div class="col-span-6 sm:col-span-6 lg:col-span-2">
              <label for="city" class="block text-sm font-medium text-gray-700"
                >City</label
              >
              <input
                type="text"
                name="city"
                id="city"
                autocomplete="address-level2"
                v-model="city"
                class="mt-1 focus:ring-indigo-500 focus:border-indigo-500 block w-full shadow-sm sm:text-sm border-gray-300 rounded-md p-1"
              />
            </div>

            <div class="col-span-6 sm:col-span-3 lg:col-span-2">
              <label
                for="region"
                class="block text-sm font-medium text-gray-700"
                >State / Province</label
              >
              <input
                type="text"
                name="region"
                id="region"
                autocomplete="address-level1"
                v-model="state"
                class="mt-1 focus:ring-indigo-500 focus:border-indigo-500 block w-full shadow-sm sm:text-sm border-gray-300 rounded-md p-1"
              />
            </div>

            <div class="col-span-6 sm:col-span-3 lg:col-span-2">
              <label
                for="postal-code"
                class="block text-sm font-medium text-gray-700"
                >ZIP / Postal code</label
              >
              <input
                type="text"
                name="postal-code"
                id="postal-code"
                autocomplete="postal-code"
                v-model="zip"
                class="mt-1 focus:ring-indigo-500 focus:border-indigo-500 block w-full shadow-sm sm:text-sm border-gray-300 rounded-md p-1"
              />
            </div>
            <div class="col-span-6 sm:col-span-3 lg:col-span-2">
              <label
                for="date-of-birth"
                class="block text-sm font-medium text-gray-700"
                >Date of Birth</label
              >
              <input
                type="date"
                name="date-of-birth"
                id="date-of-birth"
                autocomplete="postal-code"
                v-model="dob"
                class="mt-1 focus:ring-indigo-500 focus:border-indigo-500 block w-full shadow-sm sm:text-sm border-gray-300 rounded-md p-1"
              />
            </div>
            <div class="col-span-6 sm:col-span-3 lg:col-span-2">
              <label
                for="mobile-number"
                class="block text-sm font-medium text-gray-700"
                >Mobile number</label
              >
              <input
                type="tel"
                name="mobile-number"
                id="mobile-number"
                maxlength="10"
                v-model="mobileNumber"
                class="mt-1 focus:ring-indigo-500 focus:border-indigo-500 block w-full shadow-sm sm:text-sm border-gray-300 rounded-md p-1"
              />
            </div>
          </div>
        </div>
        <div class="px-4 py-3 bg-gray-50 text-right sm:px-6">
          <button
            type="submit"
            class="inline-flex justify-center py-2 px-4 border border-transparent shadow-sm text-sm font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
          >
            Create Account
          </button>
        </div>
      </div>
    </form>
  </div>
</template>

<script setup lang="ts">
import { stat } from "fs";

const firstName = ref("");
const lastName = ref("");
const email = ref("");
const password = ref("");
const confirmPassword = ref("");
const country = ref("");
const streetAddress = ref("");
const city = ref("");
const state = ref("");
const zip = ref("");
const dob = ref(null);
const mobileNumber = ref(null);

const signupFormHandler = () => {
  console.log(
    firstName.value,
    lastName.value,
    email.value,
    password.value,
    confirmPassword.value,
    country.value,
    streetAddress.value,
    city.value,
    state.value,
    zip.value,
    dob.value,
    mobileNumber.value
  );
};
</script>
