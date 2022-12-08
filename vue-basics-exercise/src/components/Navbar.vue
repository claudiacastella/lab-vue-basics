<template>
  <div id="navbar">
    <nav>
        <ul>
            <li>Home</li>
            <li>Projects</li>
            <li>Services</li>
        </ul>
    </nav>
  </div>
</template>

<script setup>

</script>

<style>
#navbar {
    position:absolute;
    top:0;
    left:0;
    width: 100%;
    background-color: blueviolet;
 }
#navbar ul {
    display: flex;
    flex-direction: row;
    row-gap: 20px;
    list-style: none;
    justify-content: space-around;
} 
#navbar ul > li {
    font-size: 24px;
    font-weight: bold;
}
</style>