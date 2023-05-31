<template>
   <div class="form-wrapper">
      <div class="container">
         <form class="form">
            <div class="input-firstName" v-if="formData.firstName">
               <p>{{ formData.firstName }}:</p>
               <input type="text" v-model="userFName" />
            </div>
            <div class="input-lastName" v-if="formData.lastName">
               <p>{{ formData.lastName }}:</p>
               <input type="text" v-model="userLName" />
            </div>
            <div class="input-birthDay" v-if="formData.birthDay">
               <p>{{ formData.birthDay }}:</p>
               <input type="date" v-model="userBirthDay" format="dd/mm/yyyy" />
            </div>
            <div class="input-number" v-if="formData.number">
               <p>{{ formData.number }}:</p>
               <input type="number" v-model="userNumber" />
            </div>
            <div class="input-email" v-if="formData.email">
               <p>{{ formData.email }}:</p>
               <input type="email" v-model="userEmail" />
            </div>
            <div class="input-userName" v-if="formData.userName">
               <p>{{ formData.userName }}:</p>
               <input type="text" v-model="userUserName" />
            </div>
            <div class="input-password" v-if="formData.password">
               <p>{{ formData.password }}:</p>
               <input type="password" v-model="userPassword" />
            </div>
            <div class="input-reEnterPassword" v-if="formData.reEnterPassword">
               <p>{{ formData.reEnterPassword }}:</p>
               <input type="password" v-model="userReEnterPassword" />
            </div>
            <div class="input-country" v-if="formData.country">
               <p>{{ formData.country }}:</p>
               <input type="text" v-model="userCountry" />
            </div>
            <div class="input-city" v-if="formData.city">
               <p>{{ formData.city }}:</p>
               <input type="text" v-model="userCity" />
            </div>
            <div class="input-address" v-if="formData.address">
               <p>{{ formData.address }}:</p>
               <input type="text" v-model="userAddress" />
            </div>
            <div class="input-zip-code" v-if="formData.zipCode">
               <p>{{ formData.zipCode }}:</p>
               <input type="text" v-model="userZipCode" />
            </div>
         </form>
      </div>
   </div>
</template>

<script setup lang="ts">
const props = defineProps<{
   formData?: any;
}>();

const userFName = ref('') as any
const userLName = ref('') as any
const userBirthDay = ref('') as any
const userNumber = ref('') as any
const userEmail = ref('') as any
const userUserName = ref('') as any
const userPassword = ref('') as any
const userReEnterPassword = ref('') as any
const userCountry = ref('') as any
const userCity = ref('') as any
const userAddress = ref('') as any
const userZipCode = ref('') as any
</script>

<style lang="scss" scoped>
@import "@/assets/scss/global.scss";
.form-wrapper {
   width: 100%;
   display: flex;
   flex-direction: row;
   justify-content: center;
   background: $bg-secondary;
   padding: 50px 0px;
}
.form {
   width: 100%;
   background: $bg;
   border-radius: 8px;
   padding: 40px;
   box-shadow: inset 0px 0px 3px 0px #b2b2b2;
   display: flex;
   flex-direction: row;
   justify-content: space-between;
   align-items: center;
   flex-wrap: wrap;
   row-gap: 30px;
   div {
      flex-basis: 48%;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      align-items: flex-start;
   }
   input {
      width: 100%;
      padding: 8px 15px;
      background: #F7F7F7;
      border-radius: 8px;
      color: #808080;
      outline: none;
      border: 1px solid #E8E8E8;
      box-shadow: 0px 0px 1px 0px #898989;
   }
   .input-address{
      flex-basis: 100%;
   }
}
</style>