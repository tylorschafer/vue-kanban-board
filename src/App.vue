<template>
  <div id="app" class="min-h-screen w-screen bg-gray-200 flex items-center justify-center">
    <ul class="w-full max-w-md">
      <li v-for="user in users" 
          :key="user.id"
          class="p-4 mb-3 flex justify-between items-center bg-white shadow rounded-lg cursor-move">
        <div class="flex items-center">
          <img class="w-10 h-10 rounded-full" :src="user.avatar" :alt="user.name">
          <p class="ml-2 text-gray-700 font-semibold font-sans tracking-wide">{{user.name}}</p>
        </div>
        <div class='flex'>
          <button aria-label='Edit User'
                  class='p-1 focus:outline-none focus:shadow-outline text-teal-500 hover:text-teal-600'
                  @click='onEdit(user)'>
                  <EditIcon/>
          </button>
          <button aria-label="Delete user"
            class="p-1 focus:outline-none focus:shadow-outline text-red-500 hover:text-red-600"
            @click="onDelete(user)">
              <Trash2Icon/>
          </button>
        </div>
        {{user.name}}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {
    EditIcon,
    Trash2Icon
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
      ],
      methods: {
        onEdit(user) {
          alert(`Editing ${user.name}`);
        },
        onDelete(user) {
          alert(`Deleting ${user.name}`);
        }
      }
    }
  }
}
</script>


