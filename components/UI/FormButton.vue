<template>
    <div class="button-wrapper">
        <!-- v-bind importa os atributos do elemento pai -->
        <!-- v-on importa os methods do elemento pai -->
        <button
          :class="[btnClass, 'button']"
          v-on="$listeners"
          v-bind="$attrs"
        >
          <slot />
        </button>
    </div>
</template>

<script>
export default {
    props: {
        btnClass: {
            type: String,
            default: ''
        }
    }
}
</script>

<style>
  .button-wrapper {
    margin: 20px;
  }

  .button {
      padding: 10px;
      border: none;
      background: darkslategray;
      color: white;
      cursor: pointer;
  }

  .button:hover {
    box-shadow: 1px 1px 5px black;
  }

  .cancel {
    background: darkred;
  }
</style>