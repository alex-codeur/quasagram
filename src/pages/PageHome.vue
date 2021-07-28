<template>
  <q-page class="contain q-pa-md">
    <div class="row q-col-gutter-lg">
      <div class="col-12 col-sm-8">
        <q-card
          v-for="post in posts"
          :key="post.id"
          class="card-post q-mb-md"
          flat
          bordered
        >
          <q-item>
            <q-item-section avatar>
              <q-avatar>
                <img
                  src="https://secure.gravatar.com/avatar/3a7e9702158dcb9a35aa8edd451913fa?s=64"
                />
              </q-avatar>
            </q-item-section>

            <q-item-section>
              <q-item-label class="text-bold">alex__esaki</q-item-label>
              <q-item-label caption>{{ post.location }}</q-item-label>
            </q-item-section>
          </q-item>

          <q-separator />

          <q-img :src="post.imageUrl" />

          <q-card-section>
            <div>{{ post.caption }}</div>
            <div class="text-caption text-grey">{{ niceDate(post.date) }}</div>
          </q-card-section>
        </q-card>
      </div>
      <div class="col-4">
        <q-item class="fixed large-screen-only">
          <q-item-section avatar>
            <q-avatar>
              <img
                src="https://secure.gravatar.com/avatar/3a7e9702158dcb9a35aa8edd451913fa?s=64"
              />
            </q-avatar>
          </q-item-section>

          <q-item-section>
            <q-item-label class="text-bold">alex__esaki</q-item-label>
            <q-item-label></q-item-label>
            <q-item-label caption>Alex Esaki</q-item-label>
          </q-item-section>
        </q-item>
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";
import { date } from "quasar";

export default defineComponent({
  name: "PageIndex",
  data() {
    return {
      posts: [
        {
          id: 1,
          caption: "Golden Date Bridge",
          date: 1627488889578,
          location: "San Francisco, United States",
          imageUrl: "https://cdn.quasar.dev/img/parallax2.jpg",
        },
        {
          id: 2,
          caption: "Golden Date Bridge",
          date: 1627488889578,
          location: "San Francisco, United States",
          imageUrl: "https://cdn.quasar.dev/img/parallax2.jpg",
        },
        {
          id: 3,
          caption: "Golden Date Bridge",
          date: 1627488889578,
          location: "San Francisco, United States",
          imageUrl: "https://cdn.quasar.dev/img/parallax2.jpg",
        },
        {
          id: 4,
          caption: "Golden Date Bridge",
          date: 1627488889578,
          location: "San Francisco, United States",
          imageUrl: "https://cdn.quasar.dev/img/parallax2.jpg",
        },
      ],
    };
  },
  methods: {
    niceDate(value) {
      return date.formatDate(value, "MMMM D h:mmA");
    },
  },
});
</script>

<style lang="sass">
.card-post
  .q-img
    min-height: 200px
</style>