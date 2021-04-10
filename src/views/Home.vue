<template>
<br>
<br>


  <h2 align="center">Inscription d'un employé</h2>

  <form style="margin-left: 34%" @submit.prevent="handelSubmit">
    <div style="width:50%" class="form-group">
      <label  for="name">Full Name</label>
      <br>
      <input
        type="text"
        class="form-control input-sm"
        id="name"
        v-model="form1.name"
        placeholder="Full Name "
      />
    </div>

    <div style="width:50%" class="form-group">
      <label for="phone">Phone</label>
      <input
        type="text"
        class="form-control"
        id="phone"
        v-model="form1.phone"
        placeholder="Phone"
      />
    </div>

    <div style="width:50%" class="form-group">
      <label for="cin">CIN</label>
      <input
        type="text"
        class="form-control"
        id="cin"
        v-model="form1.cin"
        placeholder="CIN"
      />
    </div>

    <div style="width:50%" class="form-group">
      <label for="image">Image</label>
      <input
        type="text"
        class="form-control"
        id="image"
        v-model="form1.image"
        placeholder="image"
      />
    </div>

    <div style="width:50%" class="form-group">
      <label for="address">Address</label>
      <input
        type="text"
        class="form-control"
        id="address"
        v-model="form1.address"
        placeholder="Address"
      />
    </div>

    <div style="width:50%" class="form-group">
      <label for="city">City</label>
      <input
        type="text"
        class="form-control"
        id="city"
        v-model="form1.city"
        placeholder="City"
      />
    </div>
    <br>
    <br>
    

    <button type="submit" class="btn-default">Submit</button>
  </form>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {

      form1: {

      name: "",
      phone: "",
      cin: "",
      image: "",
      address: "",
      city: "",

      }

     
    };
  },
  methods : {
    handelSubmit(){

       localStorage.setItem('form1',JSON.stringify(this.form1));
       redirect('/ProInfo')
    }
  }
};
</script>
