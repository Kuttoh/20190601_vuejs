<template>

<div>

    <input type="text" id="input" v-model="msg">

<p>Welcome Home: {{msg}}</p>

    <ul>
        <li v-for="name in names" >{{name}}</li>
    </ul>

</div>

</template>

<script>
    import Vue from 'vue'
    export default {
        data(){
            return {
                msg: 'Lion King',
                names: ['Sharon', "Sam", "PostMarlone", "Kuttoh" ]
            }
        }
    }
</script>

<style>
  input{
    color:rgb(0,107,91);
  }
</style>
