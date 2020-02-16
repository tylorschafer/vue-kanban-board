<template>
  <div id="app" class="min-h-screen w-screen bg-gray-200 flex items-center justify-center">
    <draggable
      :list="users"
      :animation="200"
      ghost-class="moving-card"
      group="users"
      filter=".action-button"
      class="w-full max-w-md"
      tag="ul"
    >
      <user-card
        v-for="user in users"
        :key="user.id"
        :user="user"
        @on-edit="onEdit"
        @on-delete="onDelete"
      ></user-card>
    </draggable>
  </div>
</template>

<script>
import draggable from "vuedraggable";
import UserCard from "./components/UserCard";
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

<style>
.moving-card {
  opacity: 0.5;
  background: #F7FAFC;
  border: 1px solid #4299e1;
}
</style>

                  
