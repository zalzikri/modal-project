
<template>
  <div  class=" align-center loader">
    <img src="/Botunify.ico" alt="Loader Icon" width="22.6px" height="22.6px" />
  </div>
</template>


<script>

export default {
  name: 'App',
  components: {
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.loader {
  position: fixed; /* Use fixed positioning to center relative to the viewport */
  top: 50%; /* Move the top edge of the loader to 50% of the viewport height */
  left: 50%; /* Move the left edge of the loader to 50% of the viewport width */
  transform: translate(-50%, -50%); /* Offset the loader by half its width and height to truly center it */
  width: 22.4px;
  height: 22.4px;
  color: #67b5e5;
  display: flex; /* Use flexbox to align the image inside the loader */
  justify-content: center; /* Center horizontally */
  align-items: center; /* Center vertically */
  z-index: -100px;
}

.loader:before {
content: '';
position: absolute;
inset: 0;
border: none;
border-radius: 100%;
background: radial-gradient(10.08px at bottom right,#0000 94%,currentColor) top left,
radial-gradient(10.08px at bottom left ,#0000 94%,currentColor) top right,
radial-gradient(10.08px at top right,#0000 94%,currentColor) bottom left,
radial-gradient(10.08px at top left ,#0000 94%,currentColor) bottom right;
background-size: 16.16px 16.16px;
background-repeat: no-repeat;
animation: loader 1.5s infinite cubic-bezier(0.3,1,0,1);
}

@keyframes loader {
33% {
inset: -8.2px;
transform: rotate(0deg);
}

66% {
inset: -8.2px;
transform: rotate(90deg);
}

100% {
inset: -5.2px;
transform: rotate(90deg);
}
}
</style>
