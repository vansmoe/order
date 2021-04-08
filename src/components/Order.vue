<template>
  <div class="wrapper"> 
    <div class="tile">
      <img class="img" src="@/assets/photo.png" alt="Profile photo">
    </div>
    <div class="job">
      <h3 class="job-title">{{ orderData.positionName }}</h3>
      <div class="job-details">
        <div class="tile job-tile">
          <img class="icon" src="@/assets/apartment.png" alt="Apartment icon">
          {{ orderData.clientNameShort }}</div>
        <div class="tile job-tile">
          <img class="icon" src="@/assets/marker.png" alt="Marker icon">
          {{ orderData.address.city }}</div>
        <div class="tile job-tile">
          <img class="icon" src="@/assets/calendar.png" alt="Calendar icon">
          {{ this.getDate(orderData.dateBegin, orderData.dateEnd) }}</div>
      </div>
    </div>
    <div class="tile highlight">{{ orderData.price }} PLN/hour</div>
    <div class="tile">
      <button class="btn-apply">Apply</button>
    </div>
  </div>
</template>

<script>
import moment from 'moment'

export default {
  name: "Order",
  props: {
    orderData: Object
  },
  methods: {
    getDate: function(dateBegin, dateEnd) {
      return `${moment(dateBegin).format("DD.MM H:mm")} - ${moment(dateEnd).format("DD.MM H:mm")}`
    } 
  }
}
</script>

<style lang="sass" scoped>

@mixin reset-button-defaults
  outline: none
  background: none
  border: 0

$primary: #2196f3

.wrapper
  max-width: 1000px
  margin: 0 auto
  padding: 20px
  display: flex
  flex-wrap: wrap
  justify-content: space-between
  align-items: center

.tile
  padding: 0 10px
  display: flex
  align-items: center
  justify-content: center
  font-size: 15px
  flex: 1 1

  @media (max-width: 800px)
    &:last-child
      flex: 1 1 100%


.job
  display: flex
  flex-wrap: wrap
  justify-content: space-between
  flex: 0 0 50%

.job-title
  margin-top: 0
  margin-left: 20px
  font-size: 20px
  font-weight: 100
  text-align: left
  flex: 1 1 100%

.job-details
  display: flex
  flex-wrap: nowrap
  align-content: center

  @media (max-width: 800px)
    flex-direction: column

.job-tile
  @media (max-width: 800px)
    justify-content: left

.icon
  max-height: 25px
  padding: 10px

.highlight
  color: $primary
  font-size: 18px
  justify-self: center

.img
  max-height: 60px

.btn-apply
  @include reset-button-defaults
  min-width: 100px
  display: block
  padding: 10px 5px
  border-radius: 5px
  background-color: $primary
  color: #fff
  font-weight: 600
  justify-self: center

  &:hover
    opacity: .7

</style>