<template>
  <div class="container">
    <div class="profile">
      <div class="avatar"></div>
      <div class="userdata">
        <strong>Ediberto Oliveira</strong>
        <span>#8370</span>
      </div>
    </div>
    <div class="actions">
      <Mic :size="20" />
      <HeadPhones :size="20" />
      <Settings :size="20" />
    </div>
  </div>
</template>

<script>
import Mic from 'vue-material-design-icons/Microphone';
import HeadPhones from 'vue-material-design-icons/Headphones';
import Settings from 'vue-material-design-icons/CogOutline';

export default {
  components: {
    Mic,
    HeadPhones,
    Settings,
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
  background: var(--quaternary);
  box-shadow: rgba(0,0,0,0.2) 0 1px 0 0;
}
.profile {
  display: flex;
  align-items: center;
}

.avatar {
  width: 32px;
  height: 32px;
  border-radius:50%;
  background: var(--grey);
}

.userdata {
  display: flex;
  flex-direction: column;
  margin-left: 8px;
  font-size: 13px;
  strong {
    display: block;
    color: var(--white);
  }

  span {
    color: var(--grey)
  }
}

.actions {
  color: var(--grey);
  span {
    cursor: pointer;
    transition:  0.2s;
    &:hover {
      color: var(--white);
    }
  }
}

</style>
