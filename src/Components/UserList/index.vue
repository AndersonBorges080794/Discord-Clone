<template>
    <div class="user-list">
        <div class="role">Disponível - 1</div>    
        <UserRow nickname="Ronaldo" isBot/>
        <div class="role">Offline - 18</div>
        <UserRow nickname="Roberto" v-for="users in 25" :key="users.id" />
        <UserRow nickname="Carlos Alberto Santos" isBot/>

    
    </div>    
</template>

<script>
import UserRow from './UserRow'


export default {
    components: {
        UserRow,
    }    
}
</script>

<style lang="scss" scoped>
.user-list{
    grid-area: UsersList;    
    display: flex;
    flex-direction: column;
    padding: 3px 6px 10px 16px;
    background-color: var(--secondary);
    max-height: calc(100vh - 46px);
    overflow-y: scroll;

    &::-webkit-scrollbar{
        width: 4px;
    }

    &::-webkit-scrollbar-thumb{
        background-color: var(--tertiary);
        border-radius: 4px;
    }

    &::-webkit-scrollbar-track{
        background-color: var(--secondary);
    }
}

.role{
    margin-top: 20px;
    color: var(--grey);
    font-weight: 500;
    font-size: 12px;
    text-transform: uppercase;
}


</style>