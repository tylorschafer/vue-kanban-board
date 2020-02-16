<template>
  <div id="app" class="min-h-screen w-screen bg-gray-200 flex items-center justify-center">
    <ul class="w-full max-w-md">
      <li v-for="user in users" 
          :key="user.id"
          class="p-4 mb-3 flex justify-between items-center bg-white shadow rounded-lg cursor-move">
        {{user.name}}
      </li>
    </ul>
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


