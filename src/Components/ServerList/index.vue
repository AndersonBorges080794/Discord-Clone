<template>
  <div class="container">
    <ServerButton isHome />
    <div class="separator"></div>
    <ServerButton :mentions="3" />
    <ServerButton hasNotification />
    <ServerButton :mentions="32" />
    <ServerButton hasNotification />
    <ServerButton :mentions="31" />
    <ServerButton hasNotification />
    <ServerButton :mentions="30" hasNotification />
  </div>
</template>


<script>
import ServerButton from "./ServerButton";
export default {
  components: {
    ServerButton
  },
};
</script>


<style lang="scss" scoped>
.container {
  grid-area: ServerList;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: var(--tertiary);
  padding: 11px 0;
  max-height: 100vh;
}

.separator {
  width: 32px;
  border-bottom: solid 2px var(--quaternary);
  margin-bottom: 8px;
}
</style>


