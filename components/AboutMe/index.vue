<template>
    <div class="aboutme">
        <div class="aboutme_cuadrocontent">
            <div class="aboutme_cuadro">
                <Icon name="fluent:brain-circuit-24-regular" class="aboutme_icon"></Icon>
                <p>Machine Learning</p>
            </div>
            <div class="aboutme_cuadro">
                <Icon name="material-symbols:terminal-sharp" class="aboutme_icon"></Icon>
                <p>Backend Developer</p>
            </div>
            <div class="aboutme_cuadro">
                <Icon name="ic:round-web" class="aboutme_icon"></Icon>
                <p>Frontend Developer</p>
            </div>
        </div>
        <div class="aboutme_model">
            <AboutMeModel/>
        </div>
        <!-- <div class="aboutme_contentcuadro"></div> -->
    </div>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
.aboutme {
    position: relative;
    padding: 15rem 10rem;

    &_cuadrocontent {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        grid-template-rows: 1fr;
        gap: 5rem;
        width: 100%;

    }
    &_cuadro {
        display: flex;
        flex-flow: column nowrap;
        justify-content: center;
        align-items: center;
        gap: 2rem;
        border-radius: 5px;
        background-image: linear-gradient(-140deg, hsl(0, 7, 5, 1), hsl(0, 0, 12, 1));
        box-shadow: 0 0 20px rgba(0, 0, 0, .7); 
        padding: 5rem 0;
        z-index: 3;
    }
    &_icon {
        height: 90px;
        width: 90px;
        color: hsl(350, 59, 47);
    }
    // &_icon:hover {
    // }
    &_model {
        position: absolute;
        top: 0;
        left: 0;

        height: 100%;
        width: 100%;
    }
    &_contentcuadro {
        height: 30rem;
        width: 100%;
        background-color: black;
    }
}

p {
    background: linear-gradient(40deg, hsl(350, 59, 47, 1), hsl(350, 59, 47, .5));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

@media screen and (max-width: 1140px) {
    .aboutme {
        padding: 8rem 5rem;

        &_model {
            top: -5rem;
        }
    }
}
@media screen and (max-width: 990px) {
    .aboutme {
        margin-top: 5rem;
        padding: 0 0;

        &_model {
            top: -5rem;
        }
    }
}
</style>