<template>
<div class="container">
    <div class="row border">
        <div  class="border" :class="col_name(columns_content)"><h1>Foo</h1></div>
        <div  class="border" :class="col_name(nav_content)"><NavBar/></div>
    </div>
    <div class="row mt-5">
        <div class="border" :class="col_name(columns_content)"></div>
        <div class="border" :class="col_name(middle_content)"><MainContent/></div>
        <div class="border" :class="col_name(columns_content)"></div>
    </div>
</div>
</template>

<script setup lang="ts">
let middle_content = 50
let columns_content = (100-middle_content) / 2
let nav_content = middle_content + columns_content
let col_name = (x:number)=> `col-${12 * (x/100)}`
</script>