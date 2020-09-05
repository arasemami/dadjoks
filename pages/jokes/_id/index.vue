<template>
  <div>
    <p class="joke">{{joke}}</p>
    <hr />
    <div>
      <span>Ref Id: {{$route.params.id}}</span>fghyhj
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      joke: "",
    };
  },
  head() {
    return {
      title: "",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "The best place fot dad jokes",
        },
      ],
    };
  },
  async created() {
    const config = {
      headers: {
        Accept: "text/plain",
      },
    };
    try {
      const res = await axios.get(
        `https://icanhazdadjoke.com/j/${this.$route.params.id}`,
        config
      );
      this.joke = res.data;
    } catch (error) {
      console.log(error);
    }
  },
};
</script>

<style scoped>
.joke {
  padding: 1rem;
  font-size: 18px;
}
</style>