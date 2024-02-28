<template>
    <div>
        <nav>
            <ul>
                <UAlert title="ทะเบียนผู้จำหน่าย" />
                <!-- <li><a class="active" href="/">Home</a></li>
                <li><a href="/about">About</a></li> -->
            </ul>
        </nav>
        <slot />


    </div>
</template>
  
<style>
body {
    margin: 0px;
}

nav>ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    overflow: hidden;
    background-color: #333;
}

nav>ul>li {
    float: left;
}

nav>ul>li a {
    display: block;
    color: white;
    text-align: center;
    padding: 14px 16px;
    text-decoration: none;
}

nav>ul>li a:hover {
    background-color: #111;
}
</style>