<template>
    <section class="myprojects">
        <div class="myproects_contenttitle">
            <h3>My Projects</h3>
            <div class="myprojects_add"></div>
        </div>
        <div class="myprojects_contentcard">
            <my-projects-card/>
        </div>
    </section>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
.myprojects {
    display: flex;
    flex-flow: column nowrap;
    gap: 12rem;
    margin: 5rem 5rem 10rem 5rem;

    &_contenttitle {
        display: flex;
        flex-flow: column nowrap;
    }
    &_add {
        position: relative;
        background-color: $secondary;
        height: 8px;
        border-radius: 20px;
        width: 25rem;

        @include neon-animation($secondary);
    }
    &_contentcard {
        display: flex;
        flex-flow: row wrap;
        justify-content: space-around;
        gap: 3rem;
    }
}
</style>