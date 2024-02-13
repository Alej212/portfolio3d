<template>
    <nav class="menubar">
        <ul class="menubar_ul">
            <li class="menubar_li">Home</li>
            <li class="menubar_li">About me</li>
            <li class="menubar_li">Projects</li>
            <li class="menubar_li">Contact me</li>
        </ul>
    </nav>
    <div id="change_mode" class="mode">
        <p>Change <br> Mode</p>
    </div>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
.menubar {
    padding-top: 2.5rem;
    padding-bottom: 2.5rem;

    &_ul {
        display: flex;
        justify-content: center;
        gap: 5rem;
    }
    // &_li {
    // }
}
.mode {
    display: none;
    position: absolute;
    top: 5rem;
    left: 1.5rem;

    padding: .8rem;
    border-radius: 5px;
    background-color: black;
    color: hsla(0, 0%, 100%, 0.4);
    text-align: center;
}
.mode:hover {
    color: hsl(0, 0%, 100%, 1);
}
</style>