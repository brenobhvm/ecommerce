<template>
  <div>
    <carrossel :items="carrosselItens" />
    <br>
    <big-cards :items="bigCardsItens" />
    <medium-cards :items="mediumCardsItens" />
    <deals :items="dealsItens" title="Deals of the Day" />
    <purchase-info-card />
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data () {
    return {
      carrosselItens: [
        { image: 'slider4.jpg', text: 'Upto 60% + Extra 10%' },
        { image: 'slider2.jpg', text: 'Upto 60% + Extra 10%' },
        { image: 'slider3.jpg', text: 'Upto 60% + Extra 10%' },
        { image: 'slider1.jpg', text: 'Upto 60% + Extra 10%' }
      ],
      bigCardsItens: [
        { image: 'slider2.jpg', text: 'Top Picks', button: { text: 'SHOP NOW', link: '/shop' } },
        { image: 'slider3.jpg', text: 'New Arrivals', button: { text: 'SHOP NOW', link: '/shop' } }
      ],
      mediumCardsItens: [
        { image: 'deal2.jpg', text: 'Lorem & Ipsum', button: { text: 'SHOP NOW', link: '/shop', icon: 'mdi-arrow-right' } },
        { image: 'deal3.jpg', text: 'Lorem & Ipsum', button: { text: 'SHOP NOW', link: '/shop', icon: 'mdi-arrow-right' } },
        { image: 'deal4.jpg', text: 'Lorem & Ipsum', button: { text: 'SHOP NOW', link: '/shop', icon: 'mdi-arrow-right' } }
      ],
      dealsItens: [
        { image: 'deal1.jpg', title: 'Bags & Purses', discount: 'Upto 60% + Extra 10%', brand: 'Baggit, Zara, Fossil', button: { text: 'EXPLORE', link: '/shop' } },
        { image: 'deal2.jpg', title: 'T-Shirt', discount: 'Upto 50%', brand: 'Zara, Selected, Celio', button: { text: 'EXPLORE', link: '/shop' } },
        { image: 'deal3.jpg', title: 'Jeans', discount: 'Upto 60% + Extra 10%', brand: 'Jack & Jones, Levis', button: { text: 'EXPLORE', link: '/shop' } },
        { image: 'deal4.jpg', title: 'Shoes', discount: 'Upto 60% + Extra 10%', brand: 'Nike, Adidas, Puma', button: { text: 'EXPLORE', link: '/shop' } }
      ]
    }
  }
}
</script>
<style>
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: .5;
  position: absolute;
  width: 100%;
}
</style>
