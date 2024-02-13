<template>
    <div class="contentfooter">
        <div class="contentfooter_contact">
            <h3>contact me</h3>
            <div class="contentfooter_linkcontent">
                <div class="contentfooter_link">
                    <a href="">
                        <Icon name="uiw:github" class="contentfooter_icon"></Icon>
                    </a>
                </div>
                <div class="contentfooter_link">
                    <a href="">
                        <Icon name="uiw:linkedin" class="contentfooter_icon"></Icon>
                    </a>
                </div>
                <div class="contentfooter_link">
                    <Icon name="" class="contentfooter_icon"></Icon>
                    <p></p>
                </div>
            </div>
        </div>
        <div class="contentfooter_model3d">
            <ContentFooterModel/>
        </div>
    </div>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
.contentfooter {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    height: 400px;

    padding-left: 5rem;
    padding-top: 5rem;
    padding-bottom: 5rem;

    // &_contact {}
    &_linkcontent {
        display: flex;
        gap: 4rem;

        padding: 5rem 0 0 2rem;
    }
    &_link {
        display: flex;
        gap: 2rem;
        align-items: center;
    }
    &_icon {
        height: 70px;
        width: 70px;
        color: $secondary;
    }
    // &_model3d {}
}

p {
    color: $secondary;
}
</style>