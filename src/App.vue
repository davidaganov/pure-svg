<template>
  <div class="wrapper">
    <header class="header">
      <h1 class="title"><strong>Pure</strong> {{ name }}</h1>
    </header>

    <section>
      <!-- First example -->
      <div class="example-wrapper">
        <h2 class="example-title">By default</h2>
        <p class="example-description">Set the icon size, alternative text, color</p>

        <div class="example-block">
          <Base-Icon :sizes="34" box="0 0 24 24" name="Email">
            <Icon-Email/>
          </Base-Icon>

          <Base-Icon :sizes="34" box="0 0 22 16" name="YouTube">
            <Icon-YouTube/>
          </Base-Icon>
        </div>
      </div>

      <!-- Second example -->
      <div class="example-wrapper">
        <h2 class="example-title">Stroke</h2>
        <p class="example-description">Sometimes you need to set a stroke for an icon, not a fill, for this you can enable the appropriate setting</p>

        <div class="example-block">
          <Base-Icon :sizes="34" box="0 0 24 24" name="Email" :stroke="true">
            <Icon-Email/>
          </Base-Icon>

          <Base-Icon :sizes="34" box="0 0 22 16" name="YouTube" :stroke="true">
            <Icon-YouTube/>
          </Base-Icon>
        </div>
      </div>

      <!-- Third example -->
      <div class="example-wrapper">
        <h2 class="example-title">Rotate</h2>
        <p class="example-description">You can set the angle of rotation of the icon</p>

        <div class="example-block">
          <Base-Icon :sizes="34" box="0 0 24 24" name="Email" :rotate="35">
            <Icon-Email/>
          </Base-Icon>

          <Base-Icon :sizes="34" box="0 0 22 16" name="YouTube" :rotate="67">
            <Icon-YouTube/>
          </Base-Icon>
        </div>
      </div>

    </section>
  </div>
</template>

<script>
import BaseIcon from "./components/BaseIcon.vue";
import IconEmail from "./components/IconEmail.vue";
import IconYouTube from "./components/IconYouTube.vue";

export default {
  name: "PureSVG",
  components: {
    BaseIcon,
    IconEmail,
    IconYouTube
  },

  data() {
    return {
      name: "SVG"
    };
  }
};
</script>

<style>
.wrapper {
  width: 80%;
  max-width: 1000px;
  margin-left: auto;
  margin-right: auto;
}

.header {
  display: flex;
  align-items: center;
}

.title {
  font: bold 32px "Roboto";
  margin-bottom: 8px;
}
.title strong {
  color: #41b883
}

.example-wrapper {
  margin-top: 40px;
}

.example-wrapper:not(:last-of-type) {
  margin-bottom: 60px;
}

.example-title {
  margin: 0;
}

.example-description {
  margin-top: 10px;
  margin-bottom: 20px;
  color: gray;
}

.example-block {
  display: grid;
  grid-auto-flow: column;
  max-width: 100px;
  align-items: center;
  color: #41b883;
}

@media (min-width: 769px) {
  .example-title {
    font: bold 26px "Roboto";
  }
  .example-description {
    font: normal 22px "Roboto";
  }
}

@media (max-width: 768px) {
  .example-title {
    font: bold 22px "Roboto";
  }
  .example-description {
    font: normal 16px "Roboto";
  }
}
</style>
