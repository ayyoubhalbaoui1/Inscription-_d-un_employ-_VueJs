<template>
  <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/ProInfo">Pro Info</router-link> |
    <router-link to="/userProfile">User Profile</router-link>
  </div>
  <router-view/>
</template>

<style>
#app {
  font-family: 'Courier New', Courier, monospace;
  color: #2c3e50;

}

#nav {
  padding: 30px;
  background-color: black;
}

#nav a {
  color: #FFF;
}

#nav a.router-link-exact-active {
  color: #fffb00;
}

</style>
