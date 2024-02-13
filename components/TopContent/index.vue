<template>
    <div class="topcontent">
        <div class="topcontent_contenttitle">
            <div class="topcontent_add"></div>
            <h2>Get to know my projects and my motivations</h2>
        </div>
        <div class="topcontent_3dscene">
            <TopContentModel/>
        </div>
    </div>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
.topcontent {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: 1fr;

    &_contenttitle {
        display: flex;
        gap: 2rem;
        padding-left: 3rem;
        margin-top: 20rem;
        margin-bottom: 15rem;
    }
    &_add {
        position: relative;
        background-color: $secondary;
        width: 20px;
        height: 100%;
        border-radius: 20px;

        @include neon-animation($secondary);
    }
//    &_3dscene {}
}
</style>