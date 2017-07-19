<template>
  <f7-page>
    <f7-navbar title="Form Storage" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block>With forms storage it is easy to store and parse forms data, especially on Ajax loaded pages. All you need to make it work is to add "store-data" class to your &lt;form&gt; and Framework7 will store form data with every input change. And the most awesome part is that when you load this page again Framework7 will parse this data and fill all form fields automatically! Just try to fill the form below and then go to any other page, or even you may close this site, and when you return here form fields will have kept your data.</f7-block>
    <f7-block-title>PERSONAL DETAILS</f7-block-title>
    <f7-list form store-data id="my-form">
      <f7-list-item>
        <f7-icon slot="media" f7="person"></f7-icon>
        <f7-label>Name</f7-label>
        <f7-input name="name" type="text" placeholder="Your name"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-icon slot="media" f7="email"></f7-icon>
        <f7-label>E-mail</f7-label>
        <f7-input name="email" type="email" placeholder="E-mail"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-icon slot="media" f7="world"></f7-icon>
        <f7-label>URL</f7-label>
        <f7-input name="url" type="url" placeholder="URL"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-icon slot="media" f7="lock"></f7-icon>
        <f7-label>Password</f7-label>
        <f7-input name="psd" type="password" placeholder="Password"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-icon slot="media" f7="phone"></f7-icon>
        <f7-label>Phone</f7-label>
        <f7-input name="tel" type="tel" placeholder="Phone"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-icon slot="media" f7="persons"></f7-icon>
        <f7-label>Gender</f7-label>
        <f7-input name="gender" type="select" v-model="selected">
          <option value="1">Male</option>
          <option value="2">Female</option>
        </f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-icon slot="media" f7="calendar"></f7-icon>
        <f7-label>Birth date</f7-label>
        <f7-input name="birth" type="date" placeholder="Birth day" value="2017-07-16"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-icon slot="media" f7="calendar"></f7-icon>
        <f7-label>Date time</f7-label>
        <f7-input name="datetime" type="datetime-local" placeholder="Birth day"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-icon slot="media" f7="check"></f7-icon>
        <f7-label>Switch</f7-label>
        <f7-input name="switch" type="switch"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-icon slot="media" f7="calendar"></f7-icon>
        <f7-label>Slider</f7-label>
        <f7-input name="slider" type="range" min="0" max="100" value="90"></f7-input>
      </f7-list-item>
      <f7-list-item class="align-top">
        <f7-icon slot="media" f7="chat"></f7-icon>
        <f7-label>About Me</f7-label>
        <f7-input name="about" type="textarea"></f7-input>
      </f7-list-item>
    </f7-list>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      selected: '1'
    }
  }
}
</script>

<style lang="less">

</style>
