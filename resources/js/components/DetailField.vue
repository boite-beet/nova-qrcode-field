<template>
    <panel-item :field="field">
      <template slot="value">
        <div class="qr-wrapper">
            <vue-qr
                class="qr-item"
                :text="field.text"
                :size="field.detailSize"
                :bgSrc="field.background"
                :logoSrc="field.logo"
                :margin="0"
            ></vue-qr>
            <p class="qr-text-value" v-if="field.showText">
              {{this.field.text}}
            </p>
        </div>
      </template>
    </panel-item>
</template>

<script>
export default {
    props: ['field'],
}
</script>

<style>
.qr-wrapper {
  display: flex;
  flex-flow: row wrap;
  align-items: center;
}

.qr-text-value {
  margin-left: .5rem;
}

.qr-item img{
    border: solid thin #ddd;
    padding: 5px;
}
</style>
