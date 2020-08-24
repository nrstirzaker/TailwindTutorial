<template>
  <div id="app">
    <div class="bg-gray-200 min-h-screen p-8 flex items-center justify-center">
      <PropertyCard :property="property"/>
    </div>
  </div>
</template>
<script>
import PropertyCard from './components/PropertyCard'
export default {
  name: 'app',
  components: {
    PropertyCard
  },
  data() {
    return {
      property:{
        imageUrl: 'https://images.unsplash.com/photo-1512917774080-9991f1c4c750',
        imageAlt: 'Rear view of modern home with pool',
        beds: 3,
        baths: 2,
        title: "Modern home in city center",
        priceInCents: 190000,
        formattedPrice: "$1,900.00",
        reviewCount: 34,
        rating: 4
      },
      popularDestinations: [
        {
          city: 'Toronto',
          averagePrice: 120,
          propertyCount: 76,
          imageUrl: '/img/toronto.jpg',
          imageAlt: 'Toronto skyline',
        },
        {
          city: 'Malibu',
          averagePrice: 215,
          propertyCount: 43,
          imageUrl: '/img/malibu.jpg',
          imageAlt: 'Cliff in Malibu',
        },
        {
          city: 'Chicago',
          averagePrice: 130,
          propertyCount: 115,
          imageUrl: '/img/chicago.jpg',
          imageAlt: 'Chicago skyline',
        },
        {
          city: 'Seattle',
          averagePrice: 135,
          propertyCount: 63,
          imageUrl: '/img/seattle.jpg',
          imageAlt: 'Seattle skyline',
        },
        {
          city: 'Colorado',
          averagePrice: 85,
          propertyCount: 47,
          imageUrl: '/img/colorado.jpg',
          imageAlt: 'Lake in Colorado',
        },
        {
          city: 'Miami',
          averagePrice: 115,
          propertyCount: 86,
          imageUrl: '/img/miami.jpg',
          imageAlt: 'Beach in Miami',
        },
      ]
    }
  }
}
</script>

<style src="./assets/tailwind.css"></style>