<template>

<div>

    <input type="text" id="input" v-model="msg">

    <p>Welcome Home: {{msg}}</p>

    <ul>
        <li v-for="name in names" v-text="name"></li>
    </ul>

    <input id="input" type="text" v-model="newName">

    <button v-on:click="addName">Add Name</button>

    <div>
        <button :title="title">Hover over me</button>
    </div>

    <div>
        <button :disabled="active" @click="toggle">Click Me</button>
    </div>

    <div>
        <ul>
            <li v-for="activity in activities" v-if="activity.completed" v-text="activity.description"></li>
        </ul>
    </div>

</div>

</template>

<script>
    export default {

        data(){
            return {
                msg: 'Lion King',
                newName: '',  //initialize variable newName
                names: ['Sharon', "Sam", "PostMarlone", "Kuttoh" ],
                title : "What are you looking for?",
                active: false,
                activities: [
                    {description: "Wake-Up", completed:true},
                    {description: "Run", completed:false}
                    ]
                }
            },

        methods:{
            addName() {
                this.names.push(this.newName) //add new name to array
                this.newName =  ''; //reset input field to blank
            },
            toggle(){
                this.active = true;
            }
        }
    }
</script>

<style>
  input{
    color:rgb(0,107,91);
  }

</style>
