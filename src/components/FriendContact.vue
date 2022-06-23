<template>
  <li>
    <h2>{{ name }}</h2>
    <button @click="toggleDetails">{{ visible ? 'Hide' : 'Show' }} Details</button>

    <ul v-if="visible">
      <li><strong>Phone:</strong> {{ phoneNumber }}</li>
      <li><strong>Email:</strong> {{ emailAddress }}</li>
    </ul>
  </li>
</template>

<script>
export default {
  props: [
    'name',
    'phoneNumber',
    'emailAddress'
  ],
  data() {
    return {
      visible: false,
      friend: {
        id: "halo",
        name: "Halo",
        phone: "123456789",
        email: "halo-demo@gmail.com",
      },
    };
  },
  methods: {
    toggleDetails() {
      this.visible = !this.visible; 
    },
  },
};
</script>

