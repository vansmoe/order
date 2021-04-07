<template>
  <div class="wrapper">
    <h3>{{ orderData.positionName }}</h3>
    <div class="details">
      <div class="tile">
        <img class="icon" src="@/assets/apartment.png" alt="Apartment icon">
        {{ orderData.clientNameShort }}</div>
      <div class="tile">
        <img class="icon" src="@/assets/marker.png" alt="Marker icon">
        {{ orderData.address.city }}</div>
      <div class="tile">
        <img class="icon" src="@/assets/calendar.png" alt="Calendar icon">
        {{ this.getDate(orderData.dateBegin, orderData.dateEnd) }}</div>
      <div class="tile highlight">
        {{ orderData.price }} PLN/hour</div>
      <button class="tile btn-apply">Apply</button>
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
  max-width: 1200px
  margin: 0 auto
  padding: 20px
  text-align: left

.details
  display: flex
  flex-wrap: wrap
  text-align: center
  justify-content: space-between

  @media (max-width: 500px)
    flex-direction: column

  @media (min-width: 800px)
    display: grid
    grid-template-columns: repeat(4, 1fr) .5fr

.tile
  display: flex
  align-items: center
  justify-content: center
  flex: 1 1 50%

.icon
  max-height: 25px
  padding: 10px

.highlight
  color: $primary
  font-size: 20px
  font-weight: 600
  justify-self: center
  

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
  flex: 1 1 100%

  &:hover
    opacity: .7

</style>