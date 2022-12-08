<template>
  <div >
    <footer id="footer">
        <div>
            <img src="" alt="" id="logo">
        </div>
        <div>
            <ul>
                <li>Home</li>
                <li>Projects</li>
                <li>Services</li>
            </ul>
        </div>
    </footer>
  </div>
</template>

<script setup>

</script>

<style>
#footer {
    position:absolute;
    bottom:0;
    left:0;
    width: 100%;
    background-color: blueviolet;
 }
#footer ul {
    display: flex;
    flex-direction: row;
    row-gap: 20px;
    list-style: none;
    justify-content: space-around;
} 
#footer ul > li {
    font-size: 24px;
    font-weight: bold;
}
</style>