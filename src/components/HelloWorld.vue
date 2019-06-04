<template>

<div>

    <input type="text" id="input" v-model="msg">

<p>Welcome Home: {{msg}}</p>

    <ul>
        <li v-for="name in names" v-text="name"></li>
    </ul>

    <input id="input" type="text" v-model="newName">

    <button v-on:click="addName">Add Name</button>

</div>

</template>

<script>
    export default {

        data(){
            return {
                msg: 'Lion King',
                newName: '',
                names: ['Sharon', "Sam", "PostMarlone", "Kuttoh" ]
            }
        },

        methods:{
            addName() {
                this.names.push(this.newName) //add new name
                this.newName =  '';
            }

        }
    }
</script>

<style>
  input{
    color:rgb(0,107,91);
  }
</style>
