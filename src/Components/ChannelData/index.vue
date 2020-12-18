<template>
    <div class="channel-data">
        <div class="messages">
            <ChannelMessage />
            <ChannelMessage />
            <ChannelMessage />
            <ChannelMessage />
            <ChannelMessage />
            <ChannelMessage />
            <ChannelMessage />
            <ChannelMessage />
            <ChannelMessage />
            <ChannelMessage />
            <ChannelMessage />
            <ChannelMessage />
            <ChannelMessage />
            <ChannelMessage />
            <ChannelMessage />
            <ChannelMessage />
            <ChannelMessage />
            <ChannelMessage />
            <ChannelMessage />
            <ChannelMessage />
            <ChannelMessage />
            <ChannelMessage />
            <ChannelMessage />
            <ChannelMessage />
            <ChannelMessage />
            <ChannelMessage />
            <ChannelMessage />
            <ChannelMessage />
        </div>
        <div class="input-wrapper">
            <input type="text" placeholder="Conversar em #chat-livre">
            <div class="icon">
                <At :size="24" />
            </div>
        </div>
    </div>   
</template>

<script>

import At from 'vue-material-design-icons/At'
import ChannelMessage from './ChannelMessage.vue'

export default {
    components:{
        At,
        ChannelMessage
    }
    
}
</script>

<style lang="scss" scoped>
.channel-data{
    grid-area: ChannelData;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    background-color: var(--primary);
    flex: 1;
}

.messages{
    display: flex;
    flex-direction: column;
    height: calc(100vh - 46px - 68px);
    max-height: calc(100vh - 46px - 68px);
    overflow-y: scroll;

    &::-webkit-scrollbar{
        width: 8px;
    }

    &::-webkit-scrollbar-thumb{
        background-color: var(--tertiary);
        border-radius: 4px;
    }

    &::-webkit-scrollbar-track{
        background-color: var(--secondary);
    }
}



.input-wrapper{
    width: 100%;
    padding: 0 16px;
    height: 68px;

    input{
        width: 100%;
        height: 44px;
        padding: 0 10px 0 57px;
        border-radius: 5px;
        color: var(--white);
        background-color: var(--chat-input);
        position: relative;

        &::placeholder{
            color: var(--grey);
        }
    }

    .icon{
        color: var(--grey);
        position: relative;
        top: -50%;
        left: 14px;
        transition: 0.2s;
        width: 24px;
    }

}


</style>