<template>
  <div>

    <body class="hero-anime">

      <div class="navigation-wrap bg-light start-header start-style">
        <div class="container">
          <div class="row">
            <div class="col-12">
              <nav class="navbar navbar-expand-md navbar-light">

                <a class="navbar-brand" href="#" target="_blank"><img src="/images/icon/QTlogo.png" alt=""></a>

                <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent"
                  aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                  <span class="navbar-toggler-icon"></span>
                </button>

                <div class="collapse navbar-collapse" id="navbarSupportedContent">
                  <ul class="navbar-nav ml-auto py-4 py-md-0">
                    <!-- <li class="nav-item pl-4 pl-md-0 ml-0 ml-md-4 active">
                      <a class="nav-link dropdown-toggle" data-toggle="dropdown" href="#" role="button"
                        aria-haspopup="true" aria-expanded="false">Home</a>
                      <div class="dropdown-menu">
                        <a class="dropdown-item" href="#">Action</a>
                        <a class="dropdown-item" href="#">Another action</a>
                        <a class="dropdown-item" href="#">Something else here</a>
                        <a class="dropdown-item" href="#">Another action</a>
                      </div>
                    </li> -->
                    <li class="nav-item pl-4 pl-md-0 ml-0 ml-md-4">
                      <nuxt-link class="nav-link" :to="{ hash: '#about' }">About</nuxt-link>
                    </li>
                    <li class="nav-item pl-4 pl-md-0 ml-0 ml-md-4">
                      <nuxt-link class="nav-link" :to="{ hash: '#timeline' }">Projects</nuxt-link>

                    </li>
                    <li class="nav-item pl-4 pl-md-0 ml-0 ml-md-4">
                      <nuxt-link class="nav-link" :to="{ hash: '#experience' }">Experience</nuxt-link>
                    </li>
                    <li class="nav-item pl-4 pl-md-0 ml-0 ml-md-4">
                      <nuxt-link class="nav-link" :to="{ hash: '#skills' }">Skills</nuxt-link>
                    </li>
                    <li class="nav-item pl-4 pl-md-0 ml-0 ml-md-4">
                      <nuxt-link class="nav-link" :to="{ hash: '#photos' }">Photos</nuxt-link>
                    </li>
                  </ul>
                </div>

              </nav>
            </div>
          </div>
        </div>
      </div>
    </body>
    <div class="container">
      <section id=about>
        <div class="slider-92911">
          <div class="owl-carousel slide-one-item">

            <div class="d-md-flex testimony-29101 align-items-stretch">
              <div class="image" style="background-image: url('/images/me/PXL_20230609_015239010.jpg');"></div>
              <div class="text">
                <blockquote>
                  <h6 id="text-des">&ldquo;I'm a developer with one year of experience as
                    an Android developer . I'm hard-working and
                    motivated, and I'm always willing to learn new
                    things.&rdquo;</h6>

                  <div class="author">&mdash; Phan Quang Thang</div>
                </blockquote>
              </div>
            </div>
          </div>

        </div>
      </section>
      <!-- <h2 class="my-5 text-center">Carousel #5</h2> -->



    </div>
    <section id=timeline>
      <h2 id="section-title">PROJECTS</h2>
      <div class="demo-card-wrapper">
        <div v-for="(project, index) in PROJECTS" :key="project" :class="`demo-card ${project.step}`">
          <div class="head">
            <div class="number-box">
              <span>{{ index + 1 }}</span>
            </div>
            <h2><span class="small">PROJECTS</span> {{ project.name }} </h2>
          </div>
          <div class="body">
            <h6>{{ project.des }}</h6>
            <img :src="`/images/projects/${project.image}`" alt="Graphic">
          </div>
        </div>
      </div>
    </section>


    <div class="container" id=experience>
        <div ><h2 id="section-title">EXPERIENCE</h2>
          <div class="timeline-item" date-is='Jun 2022 - Jun 2023'>
            <h1>ASIAN MOBILE SOFTWARE</h1>
            <h4>
              I started my programming career here as an android developer.
            </h4>
          </div></div>


    </div>
    <div class="container">
      <section id=skills>
        <h2 id="section-title">SKILLS</h2>
        <b-row>
          <b-col md="4">
            <div>
              <h2 class="skills-title">PROGRAMMING LANGUAGES</h2>
              <img  src="https://skillicons.dev/icons?i=java,kotlin,cs,css,cpp,html,vue,python&theme=light&perline=6" />
              <!-- <img v-for="image in LANGUAGES" :key="image" :src="image"
                style="width: 70px; height: 70px; object-fit: cover;" /> -->
              <!-- <b-img thumbnail v-for="image in LANGUAGES" :key="image" :src="image" width="80" fluid alt="skills image" /> -->
            </div>

          </b-col>
          <b-col md="4">
            <div>
              <h2 class="skills-title">FRAMEWORKS &amp; TOOLS </h2>
              <img  src="https://skillicons.dev/icons?i=androidstudio,django,unity,postman,nuxtjs,figma&theme=light&perline=6" />
              <!-- <b-img thumbnail v-for="image in LANGUAGES" :key="image" :src="image" width="80" fluid alt="skills image" /> -->
            </div>

          </b-col>
          <b-col md="4">
            <div>
              <h2 class="skills-title">DATABASE</h2>
              <img src="https://skillicons.dev/icons?i=sqlite,mysql&theme=light&perline=6" />  
            </div>

          </b-col>
        </b-row>
      </section>

    </div>

    <div class="container mt-1">
      <section id=photos>
        <h2 id="section-title">PHOTOS</h2>
        <div class="grid">
          <div v-for="item in MYPHOTOS" :key="item.url" :class="`card ${item.span} ${item.c}`"
            :style="`background-image: url(${item.url})`"></div>
        </div>
      </section>

    </div>
    <div class="container">
      <footer class="footer-16371">
        <div class="container">
          <div class="row justify-content-center">
            <div class="col-md-9 text-center">
              <div class="footer-site-logo mb-4">
                <a href="#">QT</a>
              </div>

              <div class="social mb-4">
                <h3>Stay in touch</h3>
                <ul class="list-unstyled">
                  <li class="in"><a href="#"><img src="/images/icon/facebook-icon-512x511-ircc9ves.png" class="icon-social" /></a></li>
                  <li class="fb"><a href="#"><img src="/images/icon/4138124.png" class="icon-social" /></a></li>
                  <li class="tw"><a href="#"><img src="/images/icon/github-512.webp" class="icon-social"/></a></li>
                  <li class="pin"><a href="#"><img src="/images/icon/4138198.png" class="icon-social"/></a></li>
                </ul>
              </div>

              <div class="copyright">
                <h6 class="mb-0"><small>&copy; 2023 - Created by QT46.</small></h6>
              </div>


            </div>
          </div>
        </div>
      </footer>
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
        { span: "span-1", c: "c-4", url: "/images/me/PXL_20221007_142156155.jpg" },
        { span: "span-1", c: "c-4", url: "/images/me/PXL_20230223_102453301.jpg" },
        { span: "span-1", c: "c-1", url: "/images/me/PXL_20230311_101713729.jpg" },
        { span: "span-1", c: "c-2", url: "/images/me/PXL_20230429_085052589.jpg" },
        // { span: "span-1", c: "c-2", url: "/images/me/PXL_20230506_104255465.jpg" },
        // { span: "span-2", c: "c-4", url: "/images/me/PXL_20230506_110309946.jpg" },
        // { span: "span-1", c: "c-4", url: "/images/me/PXL_20230506_110435112.jpg" },
        // { span: "span-2", c: "c-2", url: "/images/me/PXL_20230506_125613011.MP.jpg" },
        // { span: "span-1", c: "c-4", url: "/images/me/PXL_20230521_090207171.jpg" },
        // { span: "span-1", c: "c-4", url: "/images/me/PXL_20230528_011023785.jpg" },
        // { span: "span-3", c: "c-4", url: "/images/me/PXL_20230602_090456062~2.jpg" },
        // { span: "span-1", c: "c-1", url: "/images/me/PXL_20230609_015401216.jpg" },
        // { span: "span-2", c: "c-1", url: "/images/me/PXL_20230719_225006358.jpg" },
        // { span: "span-2", c: "c-2", url: "/images/me/PXL_20230801_095512309~2.jpg" },
        // { span: "span-1", c: "c-2", url: "/images/me/PXL_20230902_002008947~2.jpg" },

        // // { span: "span-2", c: "c-4", url: "/images/me/PXL_20230901_214607429.NIGHT.jpg" },
        // { span: "span-1", c: "c-4", url: "/images/me/PXL_20230811_104750176~3.jpg" },
        // { span: "span-1", c: "c-4", url: "/images/me/PXL_20230612_030822798.jpg" },
      ],
      PROJECTS: [
        { step: "demo-card demo-card--step1", name: "LAPTOP STORE", des: "Ecommerce Website With Django REST Framework & NuxtJs", image: "170959998-2c700593-52df-4ccf-ac58-def41a258212.png" },
        { step: "demo-card demo-card--step2", name: "PHOTO EDITOR", des: "Photo Editing App Built With Jetpack Compose ", image: "249319500-65987689-8afa-490e-b6bb-dce76e6aa01c.png" },
        { step: "demo-card demo-card--step3", name: "FRUIT-NINJA", des: "Game Fruit-Ninja built with Unity", image: "376355443_1489736278466776_7192872528555101855_n.png" },
        { step: "demo-card demo-card--step4", name: "DataMining", des: "Implement bayesian, K-means, KNN and visualization algorithms using Turtle library", image: "373364440_1429485670954303_2631368429310991096_n.png" },
        { step: "demo-card demo-card--step5", name: "COMPOSE-Self-Study", des: "Just Some UI Built with Jetpack Compose", image: "373364440_1429485670954303_2631368429310991096_n.png" },
      ],
    }
  }
}
</script>
