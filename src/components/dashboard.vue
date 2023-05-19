<template>
  <div>
   <NAVBARMENU></NAVBARMENU>
   <SidebarMenu></SidebarMenu>
  
    <div class="dashboard">
      <div class="column">
        <h2>Lorem Ipsum 1</h2>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quia illo, saepe, pariatur corporis illum architecto ipsum iusto suscipit ab deserunt quaerat ratione, perferendis cum quas? Maiores dolor corrupti eos ullam!</p>
      </div>
      <div class="column">
        <h2>Lorem Ipsum 2</h2>
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Dolore quam quod reiciendis hic asperiores. Sequi amet fugiat consequatur porro, sunt aut molestias numquam quod, autem sapiente impedit aliquam tempore quae.</p>
      </div>
      <div class="column">
        <h2>Submit Code</h2>
        <form @submit.prevent="submitCode">
          <textarea v-model="code" rows="10" cols="50" placeholder="Enter your code here"></textarea>
          <button type="submit">Submit</button>
        </form>
        <div class="camera">
          <CAMERA></CAMERA>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import NAVBARMENU from './navbar.vue';
import SidebarMenu from './HelloWorld.vue';
import CAMERA from './camera.vue'
export default {
  name:'DASHBOARD',
  components: {
    NAVBARMENU,
    SidebarMenu,
    CAMERA,
  },
  data() {
    return {
      code: ''
    };
  },
  methods: {
    submitCode() {
      
      localStorage.setItem('submittedCode', this.code);
      alert("Code Saved To Local Storage");

     
      this.code = '';
    }
  }
};
</script>

<style>
.dashboard {
  display: flex;
  margin: 50px;
  margin-left: 250px;
}

.column {
  flex: 1;
  padding: 20px;
  border-style: solid;
  border-color: rgba(0, 0, 0, 0.3);
  height: auto;
}
</style>
