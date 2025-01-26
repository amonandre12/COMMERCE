<script setup>

</script>

<template>
  <section>
    <div class="title">
        <h2>Profile</h2>
        <p>This is how others will see you on the site .</p>
      </div>
    <div class="container">
  <div>
    <div class="mb-1">
  <label for="formGroupExampleInput" class="form-label">Username</label><br>
  <input type="text" class="form-control" id="formGroupExampleInput" placeholder="shadcn">
  <p>This is your public display name. It can be your real name or a pseudonym. You can only change this once  every 30 days</p>
</div>
<div class="mb-2">
  <label for="formGroupExampleInput2" class="form-label">Email</label><br>
  <input type="email" v-model="weight" class="form-control" id="formGroupExampleInput2" placeholder="Select a verified email top display">
  <p class="para">You can manage verified email addresses in your email setting</p>
</div>
<div class="mb-3">
  <label for="exampleFormControlTextarea1" class="form-label">Bio</label><br>
  <textarea class="form-control" id="exampleFormControlTextarea1" rows="3" placeholder="I own a computer"></textarea>
  <p>You can @mention other user and organizations to link to them</p>
  </div>
<div class="links-group">
  <div class="mb-4">
  <label for="formGroupExampleInput2" class="form-label">URLs</label><br>
  <p>Add links to your website, blog, or social media profiles</p><br>
  <input type="email" v-model="weight" class="form-control" id="formGroupExampleInput2" placeholder="https://shadcn.com">
<div class="mb-5">
  <input type="email" v-model="weight" class="form-control" id="formGroupExampleInput2" placeholder="https://twitter.com/shadcn">
</div>
<button class="url">Add URL</button>
  </div>
  <div>
    <button class="btn">Update profiles</button> 
  </div>
    </div>
    </div>
    </div>
  </section>
</template>

<style lang="css" scoped>
section {
  display: flex;
}
.title {
  position: absolute;
  left: 50%;
  top: 52%;
  padding: 5px;
  border: 1px solid #ddd;
  border-radius: 8px;
  background-color: #f9f9f9;
}
.title p {
  position: relative;
  font-size: 1.2em;
  top: -13px;
}
.mb-2 label {
  position: relative;
  bottom: 7px;
  font-size: 1.2em;
}
.para {
  position: relative;
  top: -10Px;
}
.mb-2  {
  position: relative;
  top: 26px;
}
.mb-1 p {
  position: relative;
  top: -10Px;
}
.mb-3 {
  position: relative;
  top: 40px;
}
.mb-3 label {
  position: relative;
  top: 17px;
  font-size: 1.2em;
}
.mb-4 label,p {
  position: relative;
  top: 20px;
  left: 1px;
}
.links-group {
  position: relative;
  top: 87px;
  padding-bottom: 80px;
}
.mb-5 {
  position: relative;
  top: 10px;
}
.url {
  width: 100px;
  height: 40px;
  position: relative;
  top: 14px;
  font-size: 1.2em;
  border:none;
  border-radius:5px;
  padding:10px 20px ;
  font-size:14px;
  cursor:pointer;
  background-color: whitesmoke;
  color: #212E53;
  transition:background-color 0.3s;
}
.btn {
 background-color:#212E53;
 color:white;
 border:none;
 border-radius:5px;
 padding:10px 20px ;
 font-size:14px;
 cursor:pointer;
 transition:background-color 0.3s;
 position: relative;
 top: 80px;
 font-size: 1.7em;
}
.btn:hover {
 background-color:#1c7cd6;
}

.links-group input {
  width: 635px;
  height: 26px;
  padding: 5px;
}
.container {
  position: absolute;
  left: 50%;
  top: 75%;
  padding: 20px;
  border: 1px solid #ddd;
  border-radius: 8px;
  background-color: #f9f9f9;
}

textarea {
  width: 635px;
  height:105px;
  border-radius: 4px;
  border: 1px solid #ccc;
  padding: 10px;
  font-size: 14px;
  resize: none;
  position: relative;
  top: 20px;
}
.mb-1 input {
  width: 635px;
  height: 20px;
  padding: 5px;
}
.mb-1 label {
  position: relative;
  bottom: 10px;
  font-size: 1.2em;
}
.mb-2 input {
  width: 635px;
  height: 20px;
  padding: 5px;
}
</style>