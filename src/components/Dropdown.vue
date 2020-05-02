<template>
  <div class="container">
    <div class="select-box">
      <div class="options-container">
        <div class="option" v-on:click="selectDrop" v-for="item in vegetables" :key="item.name">
          <input type="radio" class="radio" name="category" />
          <label>{{item.name}}</label>
        </div>
      </div>
      <div class="selected" v-on:click="drop">Select an Item</div>
      <div class="search-box">
        <input type="text" v-on:keyup="search" autofocus placeholder="This is a search input..." />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Dropdown",
  components: {},
  data() {
    return {
        searchInput: "",
        vegetables: [
        { name: "Broccoli" },
        { name: "Lettuce" },
        { name: "Peppers" },
        { name: "Cucumber" },
        { name: "Parsley" },
        { name: "Root vegetables" }
      ]
    };
  },
  methods: {
    drop: e => {
      document.querySelector(".options-container").classList.toggle("active");
      e.target.classList.toggle("border");
      
      
    },
    selectDrop: e => {
      document.querySelector(".selected").innerHTML = e.target.innerHTML;
    },
    search: e => {
      let selected = document.querySelector(".selected");
      let searchTerm = e.target.value;
      selected.innerHTML = searchTerm;
      if (selected.innerHTML == "") {
        selected.textContent = "Select an Item";
      }
    }
  }
};
</script>

<style src="../assets/css/Dropdown.style.css">
</style>
