<template>
  <f7-page>
    <f7-navbar title="Form Elements" back-link="Forms" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block-title>FULL LAYOUT</f7-block-title>
    <f7-list form>
      <f7-list-item>
        <f7-icon slot="media" f7="person"></f7-icon>
        <f7-label>Name</f7-label>
        <f7-input type="text" placeholder="Your name"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-icon slot="media" f7="email"></f7-icon>
        <f7-label>E-mail</f7-label>
        <f7-input type="email" placeholder="E-mail"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-icon slot="media" f7="world"></f7-icon>
        <f7-label>URL</f7-label>
        <f7-input type="url" placeholder="URL"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-icon slot="media" f7="lock"></f7-icon>
        <f7-label>Password</f7-label>
        <f7-input type="password" placeholder="Password"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-icon slot="media" f7="phone"></f7-icon>
        <f7-label>Phone</f7-label>
        <f7-input type="tel" placeholder="Phone"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-icon slot="media" f7="persons"></f7-icon>
        <f7-label>Gender</f7-label>
        <f7-input type="select" v-model="selected">
          <option value="1">Male</option>
          <option value="2">Female</option>
        </f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-icon slot="media" f7="calendar"></f7-icon>
        <f7-label>Birth date</f7-label>
        <f7-input type="date" placeholder="Birth day" value="2017-07-16"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-icon slot="media" f7="calendar"></f7-icon>
        <f7-label>Date time</f7-label>
        <f7-input type="datetime-local" placeholder="Birth day"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-icon slot="media" f7="check"></f7-icon>
        <f7-label>Switch</f7-label>
        <f7-input type="switch"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-icon slot="media" f7="calendar"></f7-icon>
        <f7-label>Slider</f7-label>
        <f7-input type="range" min="0" max="100" value="90"></f7-input>
      </f7-list-item>
      <f7-list-item class="align-top">
        <f7-icon slot="media" f7="chat"></f7-icon>
        <f7-label>Textarea</f7-label>
        <f7-input type="textarea"></f7-input>
      </f7-list-item>
      <f7-list-item class="align-top">
        <f7-icon slot="media" f7="chat"></f7-icon>
        <f7-label>Resizeable</f7-label>
        <f7-input type="textarea" class="resizeable"></f7-input>
      </f7-list-item>
    </f7-list>
    <f7-block-title>ICONS AND INPUTS</f7-block-title>
    <f7-list form>
      <f7-list-item>
        <f7-icon slot="media" f7="person"></f7-icon>
        <f7-input type="text" placeholder="Your name"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-icon slot="media" f7="email"></f7-icon>
        <f7-input type="email" placeholder="E-mail"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-icon slot="media" f7="persons"></f7-icon>
        <f7-input type="select" v-model="selectedNoLabel">
          <option value="1">Male</option>
          <option value="2">Female</option>
        </f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-icon slot="media" f7="calendar"></f7-icon>
        <f7-input type="date" placeholder="Birth day" value="2017-07-16"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-icon slot="media" f7="check"></f7-icon>
        <f7-input type="switch"></f7-input>
      </f7-list-item>
    </f7-list>
    <f7-block-title>LABELS AND INPUTS</f7-block-title>
    <f7-list form>
      <f7-list-item>
        <f7-label>Name</f7-label>
        <f7-input type="text" placeholder="Your name"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-label>E-mail</f7-label>
        <f7-input type="email" placeholder="E-mail"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-label>Gender</f7-label>
        <f7-input type="select" v-model="selectedLabel">
          <option value="1">Male</option>
          <option value="2">Female</option>
        </f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-label>Birth day</f7-label>
        <f7-input type="date" placeholder="Birth day" value="2017-07-16"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-label>Switch</f7-label>
        <f7-input type="switch"></f7-input>
      </f7-list-item>
    </f7-list>
    <f7-block-title>JUST INPUTS</f7-block-title>
    <f7-list form>
      <f7-list-item>
        <f7-input type="text" placeholder="Your name"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-input type="email" placeholder="E-mail"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-input type="select" v-model="selectedJustInput">
          <option value="1">Male</option>
          <option value="2">Female</option>
        </f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-input type="date" placeholder="Birth day" value="2017-07-16"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-input type="switch"></f7-input>
      </f7-list-item>
    </f7-list>
    <f7-block-title>INSET, JUST INPUTS</f7-block-title>
    <f7-list form inset>
      <f7-list-item>
        <f7-input type="text" placeholder="Your name"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-input type="email" placeholder="E-mail"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-input type="select" v-model="selectedInset">
          <option value="1">Male</option>
          <option value="2">Female</option>
        </f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-input type="date" placeholder="Birth day" value="2017-07-16"></f7-input>
      </f7-list-item>
    </f7-list>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      selected: '1',
      selectedNoLabel: '1',
      selectedLabel: '1',
      selectedJustInput: '1',
      selectedInset: '1'
    }
  }
}
</script>

<style lang="less" scoped>
.resizeable{
  height: 43px;
}
</style>
