<template>
    <div class="card" v-for="web in webs" :key="web.number">
        <h3 class="card_number">{{ web.number }}</h3>
        <div class="card_info">
            <h6>{{ web.name }}</h6>
            <p style="color: #fff; opacity: 30%;">{{ web.resume }}</p>
        </div>
        <div class="card_link">
            <a href="">
                <Icon name="quill:link-out" class="card_icon"></Icon>
            </a>
        </div>
    </div>
</template>

<script setup lang="ts">
const webs = [
    {
        number: '01',
        name: 'ecommerce',
        resume: 'Web based on the style of the free Ecommerce market.',
        link: ''
    },
    {
        number: '02',
        name: 'movie web',
        resume: 'Application to view recent information about movies and series.',
        link: ''
    },
    {
        number: '03',
        name: 'map web',
        resume: '',
        link: ''
    }
]
</script>

<style scoped lang="scss">
.card {
    position: relative;

    display: flex;
    justify-content: center;
    align-items: flex-start;

    background-color: hsla(0,0,0,0.4);
    width: 350px;
    height: 300px;
    border-radius: 5px;
    padding-top: 3rem;
    margin-bottom: 5rem;

    &_number {
        position: absolute;
        font-size: 110px;
        top: -4.5rem;
        left: -1.5rem;
        z-index: -1;
        color: $secondary;
    }
    &_link {
        background-color: black;
        position: absolute;
        bottom: -2rem;
        right: -2rem;
        border-radius: 50%;
        padding: 1rem;
    }
    &_icon {
        height: 40px;
        width: 40px;
        color: $secondary;
    }
    &_info {
        display: flex;
        flex-flow: column nowrap;
        gap: 4rem;
        text-align: center;
        padding: 0 2rem;
    }
}
</style>