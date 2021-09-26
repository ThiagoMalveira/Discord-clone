<template>
    <div class="container">
        <div class="profile">
            <div class="avatar"></div>
            <div class="userData">
                <strong>Thiago</strong>
                <span>#8463</span>
            </div>
        </div>
        <div class="actions">
            <MicIcon :size="20" />
            <HeadphoneIcon :size="20" />
            <SettingsIcon :size="20" />
        </div>
    </div>
</template>

<script>
import MicIcon from "vue-material-design-icons/Microphone.vue";
import HeadphoneIcon from "vue-material-design-icons/Headphones.vue";
import SettingsIcon from "vue-material-design-icons/CogOutline.vue";
export default {
    components: {
        MicIcon,
        HeadphoneIcon,
        SettingsIcon
    }
}
</script>
<style lang="scss" scoped>
.container {
    grid-area: UI;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    padding: 10px;
    background-color: var(--quaternary);
    box-shadow: rgba(0,0,0,.2) 0 1px 0 0;
}
.profile{
    display: flex;
    align-items: center;
}

.avatar{ 
    width: 32px;
    height: 32px;
    border-radius: 50%;
    background-color: var(--grey);
}
.userData{
    display: flex;
    flex-direction: column;
    margin-left: 8px;
    font-size: 13px;
    strong{
        display: block;
        color: var(--white);
    }
    span{
        color: var(--grey)
    }
}
.actions{
    color: var(--grey);

    span{
        cursor: pointer;
        transition: .2s;

        &:hover{
            color: var(--white);
        }
    }
}
</style>