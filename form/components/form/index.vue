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
               <input type="date" v-model="userBirthDay" />
            </div>
            <div class="input-number" v-if="formData.number">
               <p>{{ formData.number }}:</p>
               <input type="number" v-model="userNumber" />
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
      color: #969696;
      outline: none;
      border: 1px solid #E8E8E8;
   }
}
</style>