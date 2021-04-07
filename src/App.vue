<template>
  <div id="app">
    <h3>Zadanie rekrutacyjne Adrian Krasnodębski</h3>
    <h4>07.04.2021, 10:00</h4>
    <h5 style="text-transform: uppercase">Lista ofert</h5>
    <p>
      Na podstawie dostarczonych danych utworzyć listę ofert pracy. Tak jak na
      stronie głównej incpraca.pl test
    </p>
    <ul style="text-align: left">
      <li>w folderze components należy utworzyć komponent elementu listy</li>
      <li>ikonki dostępne są w folderze assets (import ściezka wzgledna)</li>
      <li>
        Po utworzeniu komponentu listy należy utworzyć listę dla wszystkich
        ofert pracy
      </li>
      <li>
        lista wszystkich ofert ma być zawarta w komponencie OrderList tzn.
        należy wykonać import elementu listy
      </li>
      <li>
        dane wszystkich elementow listy zawarte są w komponencie OrderList
      </li>
      <li>
        w przypadku znajomosci biblioteki operującej na datach (np. moment.js -
        juz dodana do projektu) należy jej użyc przy dacie - w przeciwnym
        wypadku wystarczy sam dzien rozpoczęcia zlecenia
      </li>
    </ul>
    <OrdersList></OrdersList>
    <Exercises />
  </div>
</template>

<script>
import OrdersList from "./components/OrdersList.vue";
import Exercises from "./components/Exercises.vue";

export default {
  name: "App",
  components: {
    OrdersList,
    Exercises,
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
