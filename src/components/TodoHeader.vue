<script setup></script>

<template>
   <header>
    <nav class="container">
        <div class="branding">
            <h6>SHEROUK</h6>
        </div>
        <ul class="nav-router">
            <li>
                <RouterLink to="/">Todos</RouterLink>
            </li>
            <li>
                <RouterLink to="/about">About</RouterLink>
            </li>
        </ul>
    </nav>
   </header>
</template>

<style lang="scss" scoped>
header{
    background-color: #eee;
    nav{
        display: flex;
        justify-content: space-between;
        padding: 10px 0px;
        .branding{
            font-size: xxx-large;
            color: orange;
            font-family: system-ui;
            -webkit-text-stroke: 2px;
        }
        .nav-router{
            display: flex;
            align-self: center;
            li{
                padding: 0px 10px;
                font-size: 17px;
                font-weight: 500;
                text-transform: uppercase;
                a{
                    color: #004200;
                }
            }
        }
    }
}
</style>