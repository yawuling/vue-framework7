<template>
  <f7-page>
    <f7-navbar title="Icons" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block inner>
      <p>Framework7 comes with the premium and free <a href="https://github.com/nolimits4web/Framework7-Icons" target="_blank">Framework7 Icons</a> iOS-icons font developed specially to be used with iOS theme of Framework7. As for Material theme we recommend to use great-designed <a href="https://material.io/icons/">Material Icons</a> font. Both of these fonts use a typographic feature called <a href="http://alistapart.com/article/the-era-of-symbol-fonts"  target="_blank">ligatures</a>. It’s easy to incorporate icons into your app. Here’s a small example:</p>
      <p><code>&lt;i class="f7-icons"&gt;home&lt;/i&gt;</code> - <i class="f7-icons">home</i></p>
      <p><a href="http://alistapart.com/article/the-era-of-symbol-fonts"  target="_blank">Ligatures</a> allow rendering of an icon glyph simply by using its textual name. The replacement is done automatically by the web browser and provides more readable code than the equivalent numeric character reference.</p>
      <p>With ligatures it is also possible to combine icons like:</p>
      <p><code>&lt;i class="f7-icons"&gt;person&lt;sup&gt;add&lt;/sup&gt;&lt;/i&gt;</code> - <i class="f7-icons">person<sup>add</sup></i></p>
    </f7-block>
    <f7-block-title>IOS ICONS SET (256)</f7-block-title>
    <f7-block inner>
      <f7-grid>
        <f7-col width="33" tablet="15" class="ks-demo-icon" v-for="(icon, index) in icons" :key="index">
          <div class="icon">
            <f7-icon :f7="icon"></f7-icon>
          </div>
          <div class="icon-name">{{icon}}</div>
        </f7-col>
      </f7-grid>
    </f7-block>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      icons: [
        'add', 'add_round', 'add_round_fill', 'alarm', 'alarm_fill', 'albums', 'albums_fill', 'arrow_down', 'arrow_down_fill', 'arrow_left', 'arrow_left_fill', 'arrow_right', 'arrow_right_fill', 'arrow_up', 'arrow_up_fill', 'at', 'at_fill', 'bag', 'bag_fill', 'bars', 'bell', 'bell_fill', 'bolt', 'bolt_fill', 'bolt_round', 'bolt_round_fill', 'book', 'book_fill', 'bookmark', 'bookmark_fill', 'box', 'box_fill', 'briefcase', 'briefcase_fill', 'calendar', 'calendar_fill', 'camera', 'camera_fill', 'card', 'card_fill', 'chat', 'chat_fill', 'chats', 'chats_fill', 'check', 'check_round', 'check_round_fill', 'chevron_down', 'chevron_left', 'chevron_right', 'chevron_up', 'circle', 'circle_fill', 'circle_half', 'close', 'close_round', 'close_round_fill', 'cloud', 'cloud_download', 'cloud_download_fill', 'cloud_fill', 'cloud_upload', 'cloud_upload_fill', 'collection', 'collection_fill', 'compass', 'compass_fill', 'compose', 'compose_fill', 'data', 'data_fill', 'delete', 'delete_round', 'delete_round_fill', 'document', 'document_fill', 'document_text', 'document_text_fill', 'down', 'download', 'download_fill', 'download_round', 'download_round_fill', 'drawer', 'drawer_fill', 'drawers', 'drawers_fill', 'email', 'email_fill', 'eye', 'eye_fill', 'fastforward', 'fastforward_fill', 'fastforward_round', 'fastforward_round_fill', 'favorites', 'favorites_fill', 'film', 'film_fill', 'filter', 'filter-fill', 'flag', 'flag_fill', 'folder', 'folder_fill', 'forward', 'forward_fill', 'gear', 'gear_fill', 'graph_round', 'graph_round_fill', 'graph_square', 'graph_square_fill', 'heart', 'heart_fill', 'help', 'help_fill', 'home', 'home_fill', 'images', 'images_fill', 'info', 'info_fill', 'keyboard', 'keyboard_fill', 'layers', 'layers_fill', 'left', 'list', 'list_fill', 'lock', 'lock_fill', 'login', 'login_fill', 'logout', 'logout_fill', 'menu', 'mic', 'mic_fill', 'money_dollar', 'money_dollar_fill', 'money_euro', 'money_euro_fill', 'money_pound', 'money_pound_fill', 'money_rubl', 'money_rubl_fill', 'money_yen', 'money_yen_fill', 'more', 'more_round', 'more_round_fill', 'more_vertical', 'more_vertical_round', 'more_vertical_round_fill', 'navigation', 'navigation_fill', 'paper_plane', 'paper_plane_fill', 'pause', 'pause_fill', 'pause_round', 'pause_round_fill', 'person', 'person_fill', 'persons', 'persons_fill', 'phone', 'phone_fill', 'phone_round', 'phone_round_fill', 'photos', 'photos_fill', 'pie', 'pie_fill', 'play', 'play_fill', 'play_round', 'play_round_fill', 'radio', 'redo', 'refresh', 'refresh_round', 'refresh_round_fill', 'reload', 'reload_round', 'reload_round_fill', 'reply', 'reply_fill', 'rewind', 'rewind_fill', 'rewind_round', 'rewind_round_fill', 'right', 'search', 'search_string', 'settings', 'settings_fill', 'share', 'share_fill', 'social_facebook', 'social_facebook_fill', 'social_github', 'social_github_fill', 'social_googleplus', 'social_instagram', 'social_instagram_fill', 'social_linkedin', 'social_linkedin_fill', 'social_rss', 'social_rss_fill', 'social_twitter', 'social_twitter_fill', 'sort', 'sort_fill', 'star', 'star_fill', 'star_half', 'stopwatch', 'stopwatch_fill', 'tabs', 'tabs_fill', 'tags', 'tags_fill', 'tape', 'tape_fill', 'ticket', 'ticket_fill', 'time', 'time_fill', 'timer', 'timer_fill', 'today', 'today_fill', 'trash', 'trash_fill', 'tune', 'tune_fill', 'undo', 'unlock', 'unlock_fill', 'up', 'videocam', 'videocam_fill', 'videocam_round', 'videocam_round_fill', 'volume',  'volume_fill', 'volume_low', 'volume_low_fill', 'volume_mute', 'volume_mute_fill', 'world', 'world_fill', 'zoom_in', 'zoom_out'
      ]
    }
  }
}
</script>

<style lang="less" scoped>
code{
  background: #f3f3f3;
  padding: 5px;
}
.ks-demo-icon{
  text-align: center;
  margin-top: 15px;
  margin-bottom: 15px;
  color: #333;
  box-sizing: border-box;

  .icon-name{
    margin-top: 5px;
    font-size: 11px;
    color: #666;
  }
}
</style>
