<template>
  <div class="bg-dark h-screen">
    <div class="flex" style="height: 88vh;">
      <!-- side nav -->
      <div class="w-60 bg-black h-full flex-none">
        <div class="p-6">
        <img src="/src/assets/Spotify_Logo_RGB_White.png" class="h-10" style="filter: brightness(0) invert(1);">
        </div>
        <div class="mx-2 mb-5">
          <button v-for="page in pages" @click="setID = page.id"
                  :class="`w-full text-base font_semibold rounded px-3 py-2 flex items-center justify-start
                  ${setID === page.id ? 'bg-light text-white' : 'text-lightest'}`">
            <i class="material-icons mr-3"> {{page.icon}} </i>
            <p> {{ page.name }} </p>
          </button>
        </div>
        <div class="mx-5">
          <h1 class="mb-3 text-sm text-lightest tracking-widest uppercase">Playlist</h1>
          <button class="flex items-center justify-start opacity-75 hover:opacity-100 mb-2">
            <img src="/src/assets/plus.png" class="h-8 w-8 mr-3">
            <p class="text-sm text-white font-semibold">Create Playlist</p>
          </button>
          <button class="flex items-center justify-start opacity-75 hover:opacity-100">
            <img src="/src/assets/favorites.png" class="h-8 w-8 mr-3">
            <p class="text-sm text-white font-semibold">Liked Songs</p>
          </button>
          <div class="h-px w-full bg-light my-3"></div>

          <div class="w-full h-96 mb-3 overflow-y-scroll scroll">
            <p v-for="album in albums" class="text-lightest hover:text-white text-sm py-1"> {{ album.name }} </p>
          </div>
          <button class="flex items-center justify-start text-lightest hover:text-white">
            <i class="material-icons mr-3">download_for_offline</i>
            <p class="text-sm font-semibold">Install App</p>
          </button>
        </div>
      </div>
      <!-- main content-->
      <div class="h-full w-full relative">
        <!-- Header -->
        <div class="w-full sticky top-0 p-2">
        </div>
      </div>
    </div>
    <!-- playbar -->
    <div class="w-full bg-light" style="height: 12vh;">

    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data: function() {
    return {
      pages: [
        {id: 'home', name: 'Home', icon: 'home'},
        {id: 'search', name: 'Search', icon: 'search'},
        {id: 'library', name: 'Your Library', icon: 'bar_chart'}
      ],
      setID: 'home',
      albums: [
        {name: 'Philippe'},
        {name: 'RAP'},
        {name: 'Booska Bangers'},
        {name: 'Mélancorap'},
        {name: 'Master of Hardcore'},
        {name: 'Lyricistes'},
        {name: 'Philippe'},
        {name: 'RAP'},
        {name: 'Booska Bangers'},
        {name: 'Mélancorap'},
        {name: 'Master of Hardcore'},
        {name: 'Lyricistes'},
        {name: 'Philippe'},
        {name: 'RAP'},
        {name: 'Booska Bangers'},
        {name: 'Mélancorap'},
        {name: 'Master of Hardcore'},
        {name: 'Lyricistes'}
      ]
    };
  },
  methods: {
  }
};
</script>

<style>
</style>
