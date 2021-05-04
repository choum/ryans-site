<template>
  <div>
    <TitleCard title="Projects" icon="code" id="projects" />
    <div class="md-layout md-gutter md-alignment-center">
      <div class="join md-layout-item  md-layout md-gutter">
        <div class="md-layout-item md-size-40 md-small-size-100 img">
          <ImageCard
            :title="elc.title"
            :src="elc.src"
            :isJob="elc.isJob"
            :begin="elc.begin"
            :end="elc.end"
          />
        </div>
        <div class="md-layout-item txt">
          <TextCard :content="elc.content" :position="elc.position" />
        </div>
      </div>
    </div>
    <div class="md-layout md-gutter md-alignment-center">
      <div class="join md-layout-item  md-layout md-gutter">
        <div class="md-layout-item md-size-40 md-small-size-100 img">
          <ImageCard
            :title="pl.title"
            :src="pl.src"
            :isJob="pl.isJob"
            :begin="pl.begin"
            :end="pl.end"
          />
        </div>
        <div class="md-layout-item txt">
          <TextCard :content="pl.content" />
        </div>
      </div>
    </div>
    <div class="md-layout md-gutter md-alignment-center">
      <div class="join md-layout-item  md-layout md-gutter">
        <div class="md-layout-item md-size-40 md-small-size-100 img">
          <ImageCard :title="time.title" :src="time.src" />
        </div>
        <div class="md-layout-item txt">
          <TextCard :content="time.content" />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Vue from "vue";
import TitleCard from "./TitleCard.vue";
import ImageCard from "./ImageCard.vue";
import TextCard from "./TextCard.vue";
import VueMaterial from "vue-material";
import "vue-material/dist/vue-material.min.css";
import "vue-material/dist/theme/default.css";

Vue.use(VueMaterial);
export default {
  name: "WorkRow",
  components: { TitleCard, ImageCard, TextCard },
  data() {
    return {
      pl: {
        title: "Project Lite",
        src: require("../assets/projectlite.gif"),
        content:
          "Project Lite was the creation of me and some friends wanting to make a new, low cost smart lighting solution. The project consisted of individually addressable, hexagonal panels while could have patterns, gradients, or solid colors on them. The panels were 3d printed and used common addressable LED tape to keep costs down. A full usable interface was developed alongside the panels, and the project was entered and selected as a finalist for the Bronco Startup Challenge. While we unfortunately did not win the overall competition, we had fun developing the product. Since my friends have now graduated, we are unable to continue development on this project right now, but may do so some day."
      },
      elc: {
        title: "Embedded Lighting Controller",
        src: require("../assets/elc.png"),
        content:
          "We are designing an Embedded Lighting Controller which will use existing lighting standards to allow for easy control of different kinds of lights in embedded environments such as costumes, props, or other portable items. The device shall be simple to configure and easy to use. The device shall be able to operate under the command of a larger show control system for use in other performing arts or professional environments and also be able to operate independently for isolated works, both in professional and hobby environments. The device shall also implement a modular interface to allow selection of independent sub-modules to drive the types of lights (or other peripherals) used in that installation. This modular interface will allow users to select a driver that only does as much as they need, and potentially upgrade it should their needs change."
      },
      time: {
        title: "SVHS School Timer",
        src: require("../assets/time.png"),
        content:
          "The Silver Valley High School Bell Timer is a project I started my Junior Year of high school. The bells had broken on campus, and some people wanted to keep them off while some people wanted to keep them on. With the campus divided, I wrote this simple web app as a compromise, allowing those wishing to use the bells to have them on their computer. The web app was widely used and continues to be maintained upon request for the school. It is currently live at RyanSW.com/Timer"
      }
    };
  }
};
</script>

<style>
.md-layout {
  margin-top: 1em;
}
.img {
  padding-right: 0 !important;
}
.txt {
  padding-left: 0 !important;
}
</style>
