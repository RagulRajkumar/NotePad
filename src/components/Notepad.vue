<template>
  <div  id="Header">
    <div class="btn">
    <vs-button v-on:click="saveHandler()" class="button" type="gradient">Save</vs-button>
     <vs-button v-on:click="deleted()" class="button" color="success" type="gradient">Delete</vs-button>
    </div>
     <vs-textarea width="80%" height="400px" class="textarea" placeholder="Type here" v-model="textarea" />
  </div>
</template>
<script>
export default {
  name:'Notepad',
  
  data(){
    return{
      textarea:""
    }
  },
  methods:{
    saveHandler(){
      localStorage.setItem("pad", this.textarea);
      alert("message saved");
    },
    deleted(){
      localStorage.removeItem("pad");
      this.textarea="";
      alert("deleted successfully");
    }
  },
  mounted(){
    this.textarea= localStorage.getItem("pad");
  }
}
</script>
<style>
.button{
   margin-top: 60px;
   margin: 10px;
   
}
.textarea{
  margin: 20px 10%; 
  
}
.textarea textarea{
  height: 400px;
}
.btn{
  display: flex;
  margin-left: 10%;
}
</style>
