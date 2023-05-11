<script setup>
import { ref } from 'vue';
defineProps( {
    label: {
        type : String,
        required: true,
        default : "chich this!"
    }
})
const textInputRef = ref();
const buttonClicked = ()=> {
    alert(textInputRef.value)
    alert("Hello World!")
}
const updatebuttontext = () =>{
    textInputRef.value = "newC";
}
</script>

<template>
    <input v-model="textInputRef" type="text" placeholder="Somethings...">
    <button @click="buttonClicked">{{ label }}</button>
    <button @click="updatebuttontext">update button text</button>
</template>
