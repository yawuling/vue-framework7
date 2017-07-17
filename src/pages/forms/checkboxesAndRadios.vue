<template>
  <f7-page>
    <f7-navbar title="Checkboxes And Radios" back-link="Forms" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block-title>CHECKBOX GROUP</f7-block-title>
    <f7-list form>
      <f7-list-item checkbox name="my-checkbox" value="1" title="Books" checked></f7-list-item>
      <f7-list-item checkbox name="my-checkbox" value="2" title="Movies"></f7-list-item>
      <f7-list-item checkbox name="my-checkbox" value="3" title="Food"></f7-list-item>
      <f7-list-item checkbox name="my-checkbox" value="4" title="Drinks"></f7-list-item>
    </f7-list>
    <f7-block-title>RADIO BUTTONS GROUP</f7-block-title>
    <f7-list form>
      <f7-list-item radio name="my-radio" value="1" title="Books" checked></f7-list-item>
      <f7-list-item radio name="my-radio" value="2" title="Movies"></f7-list-item>
      <f7-list-item radio name="my-radio" value="3" title="Food"></f7-list-item>
      <f7-list-item radio name="my-radio" value="4" title="Drinks"></f7-list-item>
    </f7-list>
    <f7-block-title>WITH MEDIA LISTS</f7-block-title>
    <f7-list media-list>
      <f7-list-item
        checkbox
        name="my-checkbox-media"
        value="1"
        title="Facebook"
        subtitle="New messages from John Doe"
        text="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla sagittis tellus ut turpis condimentum, ut dignissim lacus tincidunt. Cras dolor metus, ultrices condimentum sodales sit amet, pharetra sodales eros. Phasellus vel felis tellus. Mauris rutrum ligula nec dapibus feugiat. In vel dui laoreet, commodo augue id, pulvinar lacus."
        after="17:14"
      ></f7-list-item>
      <f7-list-item
        checkbox
        name="my-checkbox-media"
        value="2"
        title="John Doe (via Twitter)"
        subtitle="John Doe (@_johndoe) mentioned you on Twitter!"
        text="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla sagittis tellus ut turpis condimentum, ut dignissim lacus tincidunt. Cras dolor metus, ultrices condimentum sodales sit amet, pharetra sodales eros. Phasellus vel felis tellus. Mauris rutrum ligula nec dapibus feugiat. In vel dui laoreet, commodo augue id, pulvinar lacus."
        after="17:14"
      ></f7-list-item>
      <f7-list-item
        checkbox
        name="my-checkbox-media"
        value="3"
        title="Facebook"
        subtitle="New messages from John Doe"
        text="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla sagittis tellus ut turpis condimentum, ut dignissim lacus tincidunt. Cras dolor metus, ultrices condimentum sodales sit amet, pharetra sodales eros. Phasellus vel felis tellus. Mauris rutrum ligula nec dapibus feugiat. In vel dui laoreet, commodo augue id, pulvinar lacus."
        after="17:14"
      ></f7-list-item>
      <f7-list-item
        checkbox
        name="my-checkbox-media"
        value="4"
        title="John Doe (via Twitter)"
        subtitle="John Doe (@_johndoe) mentioned you on Twitter!"
        text="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla sagittis tellus ut turpis condimentum, ut dignissim lacus tincidunt. Cras dolor metus, ultrices condimentum sodales sit amet, pharetra sodales eros. Phasellus vel felis tellus. Mauris rutrum ligula nec dapibus feugiat. In vel dui laoreet, commodo augue id, pulvinar lacus."
        after="17:14"
      ></f7-list-item>
    </f7-list>
    <f7-block-title>WHAT IS YOUR FAVORITE SONGS?</f7-block-title>
    <f7-list media-list>
      <f7-list-item
        radio
        value="1"
        name="my-radio-media"
        checked
        media="<img src='./static/image/photo8.jpg' width='80'/>"
        title="Yellow Submarine"
        subtitle="Don't Stop Me Now"
        text="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla sagittis tellus ut turpis condimentum, ut dignissim lacus tincidunt. Cras dolor metus, ultrices condimentum sodales sit amet, pharetra sodales eros. Phasellus vel felis tellus. Mauris rutrum ligula nec dapibus feugiat. In vel dui laoreet, commodo augue id, pulvinar lacus."
        after="$15"
      ></f7-list-item>
      <f7-list-item
        radio
        value="2"
        name="my-radio-media"
        media="<img src='./static/image/photo9.jpg' width='80'/>"
        title="Don't Stop Me Now"
        subtitle="Queen"
        text="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla sagittis tellus ut turpis condimentum, ut dignissim lacus tincidunt. Cras dolor metus, ultrices condimentum sodales sit amet, pharetra sodales eros. Phasellus vel felis tellus. Mauris rutrum ligula nec dapibus feugiat. In vel dui laoreet, commodo augue id, pulvinar lacus."
        after="$22"
      ></f7-list-item>
      <f7-list-item
        radio
        value="3"
        name="my-radio-media"
        media="<img src='./static/image/photo10.jpg' width='80'/>"
        title="Billie Jean"
        subtitle="Michael Jackson"
        text="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla sagittis tellus ut turpis condimentum, ut dignissim lacus tincidunt. Cras dolor metus, ultrices condimentum sodales sit amet, pharetra sodales eros. Phasellus vel felis tellus. Mauris rutrum ligula nec dapibus feugiat. In vel dui laoreet, commodo augue id, pulvinar lacus."
        after="$16"
      ></f7-list-item>
    </f7-list>
  </f7-page>
</template>

<script>
export default {
  
}
</script>

<style lang="less">

</style>
