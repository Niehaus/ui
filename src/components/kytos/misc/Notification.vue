<template>
  <div class="notification-container">
    <div class="k-notification">
      <div class="notification-body">
        <icon class="notification-icon" name="gear"></icon>
        <div>
          <h4 class="notification-text notification-title">Notification Title</h4>
          <p class="notification-text notification-description">Notification
            body description</p>
        </div>
      </div>
      <k-button class="dismiss-notification" tooltip="Dismiss Notification" icon="times"></k-button>
    </div>
    <hr class="notification-separator">
  </div>

</template>

<script>
import KytosBase from '../base/KytosBase';
import KytosBaseWithIcon from "../base/KytosBaseWithIcon";

export default {
  name: "k-notification",
  mixins: [KytosBaseWithIcon],
  props: {
    icon: {
      type: String,
    },
    title: {
      type: String,
    },
    description: {
      type: String,
    },
  }
}
</script>

<style lang="sass">

@import '../../../assets/styles/variables'

.notification-container
  margin: 10px

.k-notification
  display: flex
  align-items: center
  justify-content: space-between
  min-height: 80px
  margin-left: 10px
  margin-top: 10px
  margin-right: 20px
  color: $kytos-light-gray

.notification-icon
  fill: $kytos-light-gray
  width: 25px
  height: 25px
  padding: 10px
  margin-right: 5px

.notification-separator
  height: 1px
  background-color: rgba(255, 255, 255, .1)
  margin: 0px 10px
  border: none

.notification-body
  display: flex
  align-items: center

.notification-text
  margin: 10px

  &.notification-title
    font-weight: bold

  &.notification-description
    font-size: 15px


.dismiss-notification
  background: inherit !important

</style>

