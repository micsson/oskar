<template>
  <footer class="bg-black text-left py-5 mt-5">
    <div class="row">
      <div class="col">
        Built with
        <a href="https://gridsome.org/">Gridsome</a>
        <span class="font-family-headings">&amp;</span>
        <a href="https://bootstrap-vue.js.org/">BootstrapVue</a>
        <h2 class="mb-3 font-family-sans-serif h4">About</h2>
      </div>
      <div class="col">
        <p>
          Oskar Laurin is a Stockholm based designer, working in the fields of visual communication and art direction.
          MFA in Visual Communication from Konstfack.
        </p>
        <p>laurin.oskar@gmail.com</p>
        <tags-widget class="mb-5" />
        <categories-widget class="mb-5" />
      </div>
    </div>
  </footer>
</template>

 



<script>
import TagsWidget from "~/components/TagsWidget.vue";
import CategoriesWidget from "~/components/CategoriesWidget.vue";

export default {
  components: {
    TagsWidget,
    CategoriesWidget
  }
};
</script>


