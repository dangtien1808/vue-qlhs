<template>
  <aside
    id="slider"
    class="main-sidebar"
  >
    <section class="sidebar">
      <ul
        data-widget="tree"
        class="sidebar-menu"
      >
        <SlideItem
          v-for="(item,index) in slideMenuItems"
          :key="index"
          :icon="item.icon"
          :name="item.name"
          :router="item.router"
        ></SlideItem>
      </ul>
    </section>
  </aside>
</template>

<script>
import { mapGetters } from "vuex";
import SlideItem from "./SlideItem";

export default {
  name: "Slider",
  props: {
    slideMenuItems: {
      type: Array,
      default: () => []
    }
  },

  created() {},
  computed: {
    ...mapGetters(["currentUser"])
  },
  components: {
    SlideItem
  }
};
</script>

<style scrope>
.main-sidebar {
  padding-top: 70px !important;
}
</style>
