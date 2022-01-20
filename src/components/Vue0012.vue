<template>
  <div>
    <current-user>
      <template v-slot:default="{ user }">
        {{ user.age }}
      </template>
    </current-user>
  </div>
</template>

<script>
import CurrentUser from './model/CurrentUser';

export default {
  components: {
    CurrentUser,
  },
};
</script>

<style></style>
