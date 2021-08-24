<script>
  import Carousel from "components/Technologies/carouselComponent.svelte";
  import { ChevronLeftIcon, ChevronRightIcon } from "svelte-feather-icons";
  const angular = "/assets/img/technologies/angular.jpg";
  const js = "/assets/img/technologies/JavaScript.png";
  const html = "/assets/img/technologies/html.png";
  const css = "/assets/img/technologies/css.jpg";
  const typescript = "/assets/img/technologies/typescript.png";
  const react = "/assets/img/technologies/react.jpg";
  const svelte = "/assets/img/technologies/svelte_icon.jpg";
  const python = "/assets/img/technologies/python.png";
  const sass = "/assets/img/technologies/sass.png";
  const materialui = "/assets/img/technologies/material_i.png";
  const tailwind = "/assets/img/technologies/tailwind.png";
  const aws = "/assets/img/aws.png";
  const azure = "/assets/img/technologies/azure.png";
</script>

<div class="max-w-lg flex-col justify-center mx-auto">
  <Carousel perPage={3} autoplay={4000}>
    <span class="control" slot="left-control">
      <ChevronLeftIcon />
    </span>

    <div class="slide-content ">
      <img src={js} alt="JavaScript Logo" />
    </div>
    <div class="slide-content "><img src={html} alt="HTML Logo" /></div>
    <div class="slide-content "><img src={css} alt="CSS Logo" /></div>
    <div class="slide-content ">
      <img src={typescript} alt="Typescript Logo" />
    </div>
    <div class="slide-content "><img src={react} alt="React Logo" /></div>
    <div class="slide-content "><img src={angular} alt="Angular Logo" /></div>
    <div class="slide-content "><img src={svelte} alt="Svelte Logo" /></div>
    <div class="slide-content "><img src={python} alt="Python Logo" /></div>
    <div class="slide-content "><img src={sass} alt="SASS Logo" /></div>
    <div class="slide-content ">
      <img src={materialui} alt="Material UI Logo" />
    </div>
    <div class="slide-content ">
      <img src={tailwind} alt="TailwindCSS Logo" />
    </div>
    <div class="slide-content ">
      <img src={aws} alt="AWS Logo" />
    </div>
    <div class="slide-content ">
      <img src={azure} alt="Azure Logo" />
    </div>

    <span class="control" slot="right-control">
      <ChevronRightIcon />
    </span>
  </Carousel>
</div>

<style>
  .control :global(svg) {
    width: 100px;
    height: 100%;
    border-radius: 32px;
  }

  .slide-content {
    width: 40%;
    padding: 16px;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
</style>
