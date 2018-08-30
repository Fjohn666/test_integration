<template>
  <q-page class="flex flex-center q-ma-md">
    <div>
      <img src="http://buildbydesignconst.com/wp-content/uploads/2018/06/ConstructionClaimsDisputes.jpg"  style="width:100%"/>
      <div>
        <span>7 M</span><br/>
        <span>d'économies d'impots</span><br/>
        <span>en 2017</span><br/>
      </div>
    </div>
    <div>
      <q-card inline class="bigger q-ma-sm" v-for="lot in lots" :key="lot.id">
      <q-card-media>
        <img :src="lot.imageUrl">
      </q-card-media>
      <q-card-title class="relative-position">
        <q-btn fab color="primary" icon="place" class="absolute" style="top: 0; right: 8px; transform: translateY(-50%);" />

        <div class="ellipsis">{{lot.label}}</div>
        <q-rating slot="subtitle" v-model="stars" :max="lot.rating" />
        <div slot="right" class="row items-center">
          <q-icon name="place" /> {{lot.distance}}
        </div>
      </q-card-title>
      <q-card-main>
        <p>{{lot.description}}</p>
      </q-card-main>
      <q-card-separator />
      <q-card-actions>
        <q-btn flat round icon="event" />
        <q-btn flat>5:30PM</q-btn>
        <q-btn flat>7:30PM</q-btn>
        <q-btn flat>9:00PM</q-btn>
        <q-btn flat color="primary">Visiter</q-btn>
      </q-card-actions>
    </q-card>
    </div>
  </q-page>
</template>

<style>
</style>

<script>
export default {
  name: 'PageIndex',
  data () {
    return {
      lots: [
        {id: 1, imageUrl: 'https://odis.homeaway.com/odis/listing/571049c9-84f4-490a-98c7-bd827b73f12e.c10.jpg', distance: '100m', label: 'T2 vue sur mer', rating: 4, description: 'Magnifique T2 avec vue  sur la mer.'},
        {id: 2, imageUrl: 'http://www.cw-ibiza.fr/upload/12267K800_2.JPG', distance: '50 km', label: 'Villa en montagne', rating: 5, description: 'Ne soyez pas dérangé par les voisins !.'},
        {id: 3, imageUrl: 'https://www.mywanderlust.pl/wp-content/uploads/2014/02/IS_DSC_9176.jpg', distance: '1000 km', label: 'Cabane', rating: 4, description: 'Confort digne d\'un appartement parisien, pas de charges'},
        {id: 4, imageUrl: 'http://www.bet-oti.com/media/k2/items/cache/fa55c8bad0e242eb7986dc1135b50adb_XL.jpg', distance: '100m', label: 'T3 vue sur Bezons', rating: 2, description: 'Une vue sur l\'A86. Sympa non ?'},
        {id: 5, imageUrl: 'https://investinspain.be/wp-content/uploads/2018/02/modern-villa-alqueria-marbella_03-1.jpg', distance: '100m', label: 'Villa', rating: 4, description: 'Attention prévoir du temps pour faire les vitres.'}
      ]
    }
  },
  mounted () {

  }
}
</script>
