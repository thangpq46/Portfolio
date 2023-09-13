<template>
  <div>


    <section id=timeline>
      <h1>PROJECTS</h1>
      <div class="demo-card-wrapper">
        <div v-for="(project, index) in PROJECTS" :key="project" :class="`demo-card ${project.step}`">
          <div class="head">
            <div class="number-box">
              <span>{{ index + 1 }}</span>
            </div>
            <h2><span class="small">PROJECTS</span> {{ project.name }} </h2>
          </div>
          <div class="body">
            <h6 style="font-weight: 600;" >{{ project.des }}</h6>
            <!-- <p >Lorem ipsum dolor sit amet, consectetur adipisicing elit. Soluta reiciendis deserunt doloribus consequatur, laudantium odio dolorum laboriosam.</p> -->
            <img :src="`/images/projects/${project.image}`" alt="Graphic">
          </div>
        </div>
      </div>
    </section>


    <div class="container">

      <div class="timeline-item" date-is='Aug 2019'>
        <h1>UNIVERSITY OF SCIENCE AND EDUCATION (UED)</h1>
        <h4>
          I became a university student at The University of Danang - University of Science and Education
        </h4>
      </div>

      <div class="timeline-item" date-is='Jun 2022 - Jun 2023'>
        <h1>ASIAN MOBILE SOFTWARE</h1>
        <h4>
          I started my programming career here as an android developer.I wanted to explore something new so I decided to quit my job and start traveling.
        </h4>
      </div>

      <div class="timeline-item" date-is='Jul 2023'>
        <h1>GRADUATE</h1>
        <h4>
          I graduated from University of Science and Education and currently work as a freelancer.
        </h4>
      </div>

    </div>
    <b-container>
      <b-row>
        <b-col align-self="start"></b-col>
        <b-col align-self="center">SKILLS</b-col>
        <b-col align-self="end"></b-col>
      </b-row>
      <b-row>
        <b-col md="4">
          <div>
            <h2>PROGRAMMING LANGUAGES</h2>
            <img v-for="image in LANGUAGES" :key="image" :src="image"
              style="width: 70px; height: 70px; object-fit: cover;" />
            <!-- <b-img thumbnail v-for="image in LANGUAGES" :key="image" :src="image" width="80" fluid alt="skills image" /> -->
          </div>

        </b-col>
        <b-col md="4">
          <div>
            <h2>FRAMEWORKS</h2>
            <img v-for="image in LANGUAGES" :key="image" :src="image"
              style="width: 70px; height: 70px; object-fit: cover;" />
            <!-- <b-img thumbnail v-for="image in LANGUAGES" :key="image" :src="image" width="80" fluid alt="skills image" /> -->
          </div>

        </b-col>
        <b-col md="4">
          <div>
            <h2>DATABASE</h2>
            <img v-for="image in LANGUAGES" :key="image" :src="image"
              style="width: 70px; height: 70px; object-fit: cover;" />
            <!-- <b-img thumbnail v-for="image in LANGUAGES" :key="image" :src="image" width="80" fluid alt="skills image" /> -->
          </div>

        </b-col>
      </b-row>
    </b-container>

    <div class="container">
      <div class="grid">
        <div v-for="item in MYPHOTOS" :key="item.url" :class="`card ${item.span} ${item.c}`"
          :style="`background-image: url(${item.url})`"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {

  name: 'IndexPage',
  data() {
    return {
      LANGUAGES: [

        "/images/skills/compose.png",
        '/images/skills/python.jpg',
        '/images/skills/java.png',
        '/images/skills/nuxt.png',

        '/images/skills/Kotlin.png',
        '/images/skills/android.png',
        '/images/skills/cpp.png'
      ],
      MYPHOTOS: [
        { span: "span-1", c: "c-1", url: "/images/me/00000IMG_00000_BURST20190216171620973_COVER.jpg" },
        { span: "span-2", c: "c-2", url: "/images/me/2.jpg" },
        { span: "span-1", c: "c-2", url: "/images/me/20210421_145053.jpg" },
        { span: "span-2", c: "c-4", url: "/images/me/20230814_084612_497.jpg" },
        { span: "span-1", c: "c-4", url: "/images/me/a.jpg" },
        { span: "span-1", c: "c-5", url: "/images/me/c.jpg" },
        { span: "span-2", c: "c-2", url: "/images/me/d.jpg" },
        { span: "span-1", c: "c-5", url: "/images/me/e.jpg" },
        { span: "span-1", c: "c-5", url: "/images/me/E7D_1261~2.JPG" },
        { span: "span-1", c: "c-2", url: "/images/me/f.jpg" },
        { span: "span-1", c: "c-2", url: "/images/me/g.jpg" },
        { span: "span-3", c: "c-1", url: "/images/me/IMG_20230816_062046_832.webp" },
        { span: "span-2", c: "c-2", url: "/images/me/IMG_5680.JPG" },
        { span: "span-2", c: "c-2", url: "/images/me/IMG_20190216_163545.jpg" },
        { span: "span-1", c: "c-4", url: "/images/me/E7D_1261~2.JPG" },
        { span: "span-1", c: "c-4", url: "/images/me/IMG_1688532535572_1688554125022~2.jpg" },
        { span: "span-2", c: "c-1", url: "/images/me/IMG_1688532535592_1688554132064~3.jpg" },
        { span: "span-1", c: "c-2", url: "/images/me/original_91144d98-a737-40da-9d42-7693b9e30cef_PXL_20230908_110045522.jpg" },
        { span: "span-1", c: "c-2", url: "/images/me/PXL_20220916_224510370.jpg" },
        { span: "span-1", c: "c-4", url: "/images/me/PXL_20220917_223208400.MP.jpg" },
        { span: "span-2", c: "c-4", url: "/images/me/PXL_20221007_142156155.jpg" },
        { span: "span-1", c: "c-4", url: "/images/me/PXL_20230223_102453301.jpg" },
        { span: "span-1", c: "c-1", url: "/images/me/PXL_20230311_101713729.jpg" },
        { span: "span-1", c: "c-2", url: "/images/me/PXL_20230429_085052589.jpg" },
        { span: "span-1", c: "c-2", url: "/images/me/PXL_20230506_104255465.jpg" },
        { span: "span-2", c: "c-4", url: "/images/me/PXL_20230506_110309946.jpg" },
        { span: "span-1", c: "c-4", url: "/images/me/PXL_20230506_110435112.jpg" },
        // { span: "span-2", c: "c-2", url: "/images/me/PXL_20230506_125613011.MP.jpg" },
        { span: "span-1", c: "c-4", url: "/images/me/PXL_20230521_090207171.jpg" },
        { span: "span-1", c: "c-4", url: "/images/me/PXL_20230528_011023785.jpg" },
        // { span: "span-3", c: "c-4", url: "/images/me/PXL_20230602_090456062~2.jpg" },
        // { span: "span-1", c: "c-1", url: "/images/me/PXL_20230609_015401216.jpg" },
        // { span: "span-2", c: "c-1", url: "/images/me/PXL_20230719_225006358.jpg" },
        // { span: "span-2", c: "c-2", url: "/images/me/PXL_20230801_095512309~2.jpg" },
        // { span: "span-1", c: "c-2", url: "/images/me/PXL_20230902_002008947~2.jpg" },

        // // { span: "span-2", c: "c-4", url: "/images/me/PXL_20230901_214607429.NIGHT.jpg" },
          { span: "span-1", c: "c-4", url: "/images/me/PXL_20230811_104750176~3.jpg" },
          { span: "span-1", c: "c-4", url: "/images/me/PXL_20230612_030822798.jpg" },
      ],
      PROJECTS: [
        { step: "demo-card demo-card--step1", name: "LAPTOP STORE", des: "Ecommerce Website With Django REST Framework & NuxtJs", image: "170959998-2c700593-52df-4ccf-ac58-def41a258212.png" },
        { step: "demo-card demo-card--step2", name: "PHOTO EDITOR", des: "Photo Editing App Built With Jetpack Compose.This is my final year project. ", image: "249319500-65987689-8afa-490e-b6bb-dce76e6aa01c.png" },
        { step: "demo-card demo-card--step3", name: "FRUIT-NINJA", des: "Game Fruit-Ninja. I built it while learning unity on my own. ", image: "376355443_1489736278466776_7192872528555101855_n.png" },
        { step: "demo-card demo-card--step4", name: "DataMining", des: "Implement bayesian, K-means, KNN and visualization algorithms using Turtle library", image: "Untitled.png" },
        { step: "demo-card demo-card--step5", name: "COMPOSE-Self-Study", des: "Just some UI built with Jetpack Compose. Build to learn more about the Jetpack library", image: "373364440_1429485670954303_2631368429310991096_n.png" },
      ],
    }
  }
}
</script>
