<template>
  <div id="app" class="min-h-screen w-screen bg-gray-200 flex items-center justify-center">

  </div>
</template>

<script>
export default {
  name: "App",
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
      ]
    }
  },
  methods: {
    onEdit(user) {
      alert(`Editing ${user.name}`);
    },
    onDelete(user) {
      alert(`Deleting ${user.name}`);
    }
  }
};
</script>

                  
