<template>
  <div class="md-layout md-gutter" id="wrapper">
    <div class="md-layout-item md-size-25">
      <md-card id="info">
        <md-card-header>
          <div id="icon">
            <md-avatar class="md-large">
              <img src="../assets/profile.png" />
            </md-avatar>
          </div>
        </md-card-header>
        <h1 class="md-display-2">Ryan White</h1>
        <p class="md-subheading">Computer Engineer</p>

        <md-list>
          <md-list-item>
            <md-icon>work</md-icon>
            <a
              v-smooth-scroll
              href="#work"
              style="color: #3f4238"
              class="md-list-item-text"
              >Work History</a
            >
          </md-list-item>
          <md-list-item>
            <md-icon>code</md-icon>
            <a
              v-smooth-scroll
              href="#projects"
              style="color: #3f4238"
              class="md-list-item-text"
              >Projects</a
            >
          </md-list-item>
        </md-list>
        <SocialLinks />
      </md-card>
    </div>
    <div class="md-layout-item">
      <WorkRow />
      <ProjectRow />
    </div>
  </div>
</template>

<script>
import Vue from "vue";
import VueMaterial from "vue-material";
import SocialLinks from "./SocialLinks.vue";
import WorkRow from "./WorkRow.vue";
import ProjectRow from "./ProjectRow.vue";
import "vue-material/dist/vue-material.min.css";
import "vue-material/dist/theme/default.css";
import VueSmoothScroll from "vue2-smooth-scroll";
Vue.use(VueSmoothScroll);
Vue.use(VueMaterial);

export default {
  name: "Content",
  components: { SocialLinks, WorkRow, ProjectRow }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.bottom {
  align-items: flex-end;
}
.is-active {
  color: white;
}
#wrapper {
  margin-top: 2em;
  margin-left: 5em;
  margin-right: 5em;
}
.md-avatar {
  min-width: 175px !important;
  min-height: 175px !important;
  border-radius: 175px !important;
  margin-right: 0px;
  margin-left: 0px;
  align-items: center;
}

#info {
  background-color: var(--seashell);
  position: sticky;
  top: 0;
  padding-bottom: 1.5em;
}

.md-content {
  border: none;
  overflow: hidden !important;
}

.md-list {
  background-color: var(--seashell);
  margin-bottom: 5em;
}

.md-list-item {
  background-color: var(--seashell);
}
.md-list-item-text {
  font-size: 20px;
}

#icon {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 2em;
}
h1 {
  text-align: center;
  margin-bottom: 0.2em;
}
h2 {
  margin-left: 1.2em;
}
p {
  text-align: center;
  font-style: italic;
}

i {
  font-size: 40px !important;
  padding-left: 1.3em;
}

a:hover {
  color: red;
}
</style>
