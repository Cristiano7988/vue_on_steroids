<template>
    <div class="field-wrapper">
        <label><slot /></label>
        <input
          :value="value"
          v-if="!type"
          type="text"
          @input="$emit('input', $event.target.value)"
        />
        <textarea
          :value="value"
          v-if="type === 'textarea'"
          @input="$emit('input', $event.target.value)"
        />
    </div>
</template>

<script>
export default {
    props: {
        type: {
            type: String,
            default: ''
        },
        value: {
            type: String,
            default: ''
        }
    }
}
</script>

<style>
  .field-wrapper label {
    font-family: 'Aboreto';
    font-weight: bold;
    font-size: 11px;
    text-shadow: .1px .1px .1px black;
  }
  .field-wrapper {
    padding: 10px;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  }

  .field-wrapper input, .field-wrapper textarea {
    width: 100%;
  } 
</style>