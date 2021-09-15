<template>
  <section>
       <b-table
            :data="hotels"
            :selected.sync="selected"
            paginated
            per-page=10                        
            aria-next-label="Next page"
            aria-previous-label="Previous page"
            aria-page-label="Page"
            aria-current-label="Current page">

            <b-table-column field="name" label="Name" sortable  v-slot="props">
                {{ props.row.name }}
            </b-table-column> 
            
             <b-table-column field="city" label="City" sortable  v-slot="props">
                {{ props.row.city }}
            </b-table-column>  
            
            <b-table-column field="country" label="Country" sortable  v-slot="props">
                {{ props.row.country }}
            </b-table-column>            
            
            <b-table-column field="price" label="Price" width="40" sortable numeric v-slot="props">
                {{ props.row.price }}
            </b-table-column>
            
             <b-table-column field="stars" label="Stars" width="40" sortable numeric v-slot="props">
                {{ props.row.stars }}
            </b-table-column>            

        </b-table>
  </section>
</template>

<script>
import { MessageBus } from "@podium/browser";
const messageBus = new MessageBus();

export default {
  name: 'HotelList',
  props: {
    msg: String
  },
  data:()=> ({
      selected: null,
    hotels: [{
id: "92ebb121-d823-4ffe-a836-3c70b4faad18",
name: "iusto cumque delectus",
country: "Bangladesh",
city: "Port Marisolhaven",
price: 263,
images: [
"http://lorempixel.com/640/480/city?46815",
"http://lorempixel.com/640/480/city?70019",
"http://lorempixel.com/640/480/city?27220",
"http://lorempixel.com/640/480/city?45497",
"http://lorempixel.com/640/480/city?30330",
"http://lorempixel.com/640/480/city?1331",
"http://lorempixel.com/640/480/city?81254"
],
date_start: "2021-09-06T10:44:35.541Z",
date_end: "2022-03-12T06:10:35.381Z",
stars: 5,
rating: 1.5207276869589959,
description: "Corrupti nostrum ut illo. Id voluptas sit consectetur itaque maxime ea omnis sed. Quibusdam voluptatum nobis dolor illo nobis. Accusamus harum velit eum quis aperiam velit et in. In placeat et. Officia in mollitia repudiandae exercitationem et."
},
{
id: "43bbaa13-edf7-4f3e-9bb3-bad435b9dd26",
name: "deserunt consequatur dolor",
country: "United States of America",
city: "Lake Tyra",
price: 837,
images: [
"http://lorempixel.com/640/480/city?42167",
"http://lorempixel.com/640/480/city?24399",
"http://lorempixel.com/640/480/city?8274",
"http://lorempixel.com/640/480/city?49721",
"http://lorempixel.com/640/480/city?10331",
"http://lorempixel.com/640/480/city?22035",
"http://lorempixel.com/640/480/city?39856"
],
date_start: "2021-09-06T10:44:35.541Z",
date_end: "2021-11-20T18:05:43.939Z",
stars: 1,
rating: 3.8215364452992846,
description: "Sit et sed aut consequatur totam. Sapiente deserunt voluptas. Velit reprehenderit cupiditate enim non voluptate qui sequi possimus hic. Qui ipsum voluptatibus eius quis magnam minima laboriosam cum. Maiores temporibus fugit ducimus. Voluptatum consequatur blanditiis dolores odit rerum nobis unde deserunt."
},
{
id: "31c25505-86e3-42e2-8fad-944d00ce5e64",
name: "ab odio quia",
country: "Ukraine",
city: "Josueburgh",
price: 104,
images: [
"http://lorempixel.com/640/480/city?17269",
"http://lorempixel.com/640/480/city?61088",
"http://lorempixel.com/640/480/city?42404",
"http://lorempixel.com/640/480/city?45268",
"http://lorempixel.com/640/480/city?63722"
],
date_start: "2021-09-06T10:44:35.541Z",
date_end: "2022-06-07T23:34:39.861Z",
stars: 3,
rating: 1.6544192704166174,
description: "Aut impedit repudiandae quis id. Esse maxime sapiente omnis ullam. Nam et qui odio est et aut consequatur ea ea."
},
{
id: "94eda8a2-7a4b-4df9-80f5-1bf9aba2a782",
name: "repellendus quas fuga",
country: "Chile",
city: "West Athenaview",
price: 521,
images: [
"http://lorempixel.com/640/480/city?46752",
"http://lorempixel.com/640/480/city?75821"
],
date_start: "2021-09-06T10:44:35.541Z",
date_end: "2022-05-12T12:31:08.583Z",
stars: 5,
rating: 5.551340028436979,
description: "Officia soluta voluptatem et. Quia nemo aut. Delectus qui soluta nihil praesentium totam et animi ut. Nostrum autem sit sunt voluptatem sed enim ipsam ea."
},
{
id: "cca507ea-5d9a-4412-88cf-4ba3f3d8486c",
name: "numquam velit architecto",
country: "Tanzania",
city: "North Eva",
price: 297,
images: [
"http://lorempixel.com/640/480/city?27451",
"http://lorempixel.com/640/480/city?80447",
"http://lorempixel.com/640/480/city?25248",
"http://lorempixel.com/640/480/city?98129",
"http://lorempixel.com/640/480/city?47118",
"http://lorempixel.com/640/480/city?29333",
"http://lorempixel.com/640/480/city?11601",
"http://lorempixel.com/640/480/city?41837",
"http://lorempixel.com/640/480/city?72819"
],
date_start: "2021-09-06T10:44:35.541Z",
date_end: "2022-07-22T17:49:03.122Z",
stars: 1,
rating: 2.1152513528141412,
description: "Tenetur id et magni distinctio sed rerum deserunt. Voluptatem quo temporibus animi dolor porro tempore. Inventore maxime ad non voluptate inventore a est fuga. Ex animi ea. Ut dolorem harum qui. Dolor porro deleniti sit voluptatum animi ut."
},
{
id: "1b3a2f88-0ff8-47f0-81fb-aecef549bd43",
name: "vitae qui unde",
country: "Egypt",
city: "Turnerbury",
price: 441,
images: [
"http://lorempixel.com/640/480/city?18242",
"http://lorempixel.com/640/480/city?58989",
"http://lorempixel.com/640/480/city?74525",
"http://lorempixel.com/640/480/city?24471",
"http://lorempixel.com/640/480/city?5661",
"http://lorempixel.com/640/480/city?26940",
"http://lorempixel.com/640/480/city?17177"
],
date_start: "2021-09-06T10:44:35.541Z",
date_end: "2021-09-07T20:45:46.232Z",
stars: 4,
rating: 3.4502045995974786,
description: "Nostrum vel quis asperiores magni veniam nobis nemo in. Rerum labore sapiente consequatur est ea reiciendis officiis. Enim aut eos dolor sit fuga cumque consequuntur eveniet. Sed et quis debitis minima nihil atque saepe nemo molestias. Voluptas et ducimus eum voluptate et tenetur consequatur corrupti quaerat. Dolorem et ut accusamus perferendis."
}],
  }),
  mounted: function() {
    messageBus.subscribe("internalchannel", "hotels", event => {
      this.hotels = event.payload.hotels;
    });   
  },
  watch: {    
    selected: function (newDetail) {      
      messageBus.publish('internalchannel', 'hotel-detail', {message: 'hotel-detail', from: 'vue hotel list', hotel: newDetail});
      this.$emit('hotel','hotel-detail')
      console.log('emit event: hotel-detail', newDetail)
    }    
  },
}
</script>


