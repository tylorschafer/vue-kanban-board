<template>
  <div id="app" class="min-h-screen w-screen bg-gray-200 flex items-center justify-center">
    <ul class="w-full max-w-md">
      <li v-for="user in users" 
          :key="user.id"
          class="p-4 mb-3 flex justify-between items-center bg-white shadow rounded-lg cursor-move">
        {{user.name}}
      </li>
    </ul>
    <div class="flex items-center">
      <img class="w-10 h-10 rounded-full" :src="user.avatar" :alt="user.name">
      <p class="ml-2 text-gray-700 font-semibold font-sans tracking-wide">{{user.name}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {
  },
  data() {
    return {
      users: [
        {
          id: 1,
          name: "Lady GaGa",
          avatar: "https://pickaface.net/gallery/avatar/judycsmosh521a551b604bf.png"
        },
        {
          id: 2,
          name: "Johnny Depp",
          avatar: "https://pickaface.net/gallery/avatar/gs315535348ce076c6.png"
        },
        {
          id: 3,
          name: "Steve Jobs",
          avatar: "https://pickaface.net/gallery/avatar/Opi51c74d0125fd4.png"
        }
      ]
    }
  }
}
</script>


