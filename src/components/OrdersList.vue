<template>
  <div>
    <Order v-for="order in ordersData" :key="order.orderId" :order-data="order" />
  </div>
</template>

<script>
import Order from "./Order"

export default {
  name: "OrdersList",
  components: {
    Order
  },
  data() {
    return {
      ordersData: [
        {
          orderId: 153401,
          clientNameShort: '"MEDIGEN"',
          dateBegin: "2021-04-07T08:00:00",
          dateEnd: "2021-04-07T16:00:00",
          positionName: "Leasing personalny",
          price: 20.0,
          address: {
            country: {
              id: "PL",
              countryName: "Poland",
              localCountryName: "Polska",
            },
            city: "Warszawa",
            street: "ul. Gustawa Morcinka",
            houseNumber: "5",
            apartmentNumber: "19/21",
            postalCode: "01-496",
            province: { id: 7, name: "Mazowieckie" },
            gmina: "Bemowo",
            powiat: { id: 441, name: "Warszawa" },
          },
        },
        {
          orderId: 153403,
          clientNameShort: '"MEDIGEN"',
          dateBegin: "2021-04-09T08:00:00",
          dateEnd: "2021-04-09T16:00:00",
          positionName: "Leasing personalny",
          price: 20.0,
          address: {
            country: {
              id: "PL",
              countryName: "Poland",
              localCountryName: "Polska",
            },
            city: "Warszawa",
            street: "ul. Gustawa Morcinka",
            houseNumber: "5",
            apartmentNumber: "19/21",
            postalCode: "01-496",
            province: { id: 7, name: "Mazowieckie" },
            gmina: "Bemowo",
            powiat: { id: 441, name: "Warszawa" },
          },
        },
        {
          orderId: 153404,
          clientNameShort: '"MEDIGEN"',
          dateBegin: "2021-04-10T08:00:00",
          dateEnd: "2021-04-10T16:00:00",
          positionName: "Leasing personalny",
          price: 20.0,
          address: {
            country: {
              id: "PL",
              countryName: "Poland",
              localCountryName: "Polska",
            },
            city: "Warszawa",
            street: "ul. Gustawa Morcinka",
            houseNumber: "5",
            apartmentNumber: "19/21",
            postalCode: "01-496",
            province: { id: 7, name: "Mazowieckie" },
            gmina: "Bemowo",
            powiat: { id: 441, name: "Warszawa" },
          },
        },
        {
          orderId: 153410,
          clientNameShort: "Biedronka",
          clientLogoFileId: 204548,
          dateBegin: "2021-04-11T07:00:00",
          dateEnd: "2021-04-11T15:00:00",
          positionName: "Outsourcing personalny",
          price: 18.3,
          address: {
            country: {
              id: "PL",
              countryName: "Poland",
              localCountryName: "Polska",
            },
            city: "Warszawa",
            street: "Kijowska",
            houseNumber: "20",
            postalCode: "03-743",
            province: { id: 7, name: "Mazowieckie" },
            gmina: "Warszawa",
            powiat: { id: 441, name: "Warszawa" },
          },
        },
        {
          orderId: 153405,
          clientNameShort: '"MEDIGEN"',
          dateBegin: "2021-04-11T08:00:00",
          dateEnd: "2021-04-11T16:00:00",
          positionName: "Leasing personalny",
          price: 20.0,
          address: {
            country: {
              id: "PL",
              countryName: "Poland",
              localCountryName: "Polska",
            },
            city: "Warszawa",
            street: "ul. Gustawa Morcinka",
            houseNumber: "5",
            apartmentNumber: "19/21",
            postalCode: "01-496",
            province: { id: 7, name: "Mazowieckie" },
            gmina: "Bemowo",
            powiat: { id: 441, name: "Warszawa" },
          },
        },
      ],
    };
  },
};
</script>

<style>
</style>