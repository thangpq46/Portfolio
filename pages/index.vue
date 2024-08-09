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
              <div class="image" style="background-image: url('/images/me/PXL_20240714_112733772.jpg');"></div>
              <div class="text">
                <blockquote>
                  <h6 id="text-des">&ldquo;Android Developer with two years of experience, skilled in working independently to deliver high-quality mobile apps. Proactive in learning new technologies and driven to create efficient, user-friendly applications.&rdquo;</h6>

                  <div class="author">&mdash; Phan Quang Thang</div>
                </blockquote>
              </div>
            </div>
          </div>

        </div>
      </section>
      <!-- <h2 class="my-5 text-center">Carousel #5</h2> -->



    </div>

    <section id="timeline" class="my-5">
  <h2 id="section-title" class="text-center mb-4">PERSONAL PROJECT
  </h2>
  <div class="container">
    <div class="row">
      <div
        v-for="(project, index) in PROJECTS"
        :key="index"
        class="col-md-6 mb-4"
      >
        <div class="card h-100 border-0 shadow-sm" style="border-radius: 20px;">
          <div class="card-header bg-primary text-white" style="border-radius: 20px 20px 0 0;">
            <h5 class="mb-0">{{ project.name }}</h5>
          </div>
          <div class="card-body d-flex flex-column" style="border-radius: 0 0 20px 20px;">
            <h6 class="card-text text-dark flex-grow-1">{{ project.des }}</h6>
            <div class="mt-3">
              <h6 class="font-weight-bold">Technologies Used:</h6>
              <ul class="list-unstyled">
                <li v-for="(tech, techIndex) in project.technologies" :key="techIndex" class="badge badge-pill badge-info mr-2 mb-2">{{ tech }}</li>
              </ul>
            </div>
            <a :href="project.purl" class="btn btn-outline-primary mt-3 align-self-start" target="_blank" rel="noopener noreferrer">
              View Project
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- 
    <section id="timeline" class="my-5">
  <h2 id="section-title" class="text-center mb-4">Projects</h2>
  <div class="container">
    <div class="row">
      <div
        v-for="(project, index) in PROJECTS"
        :key="index"
        class="col-md-6 mb-4"
      >
        <div class="card h-100 border-0 shadow-sm" style="border-radius: 20px;">
          <div class="card-header bg-primary text-white" style="border-radius: 20px 20px 0 0;">
            <h5 class="mb-0">{{ project.name }}</h5>
          </div>
          <div class="card-body d-flex flex-column" style="border-radius: 0 0 20px 20px;">
            <h6 class="card-text text-dark flex-grow-1">{{ project.des }}</h6>
            <a :href="project.purl" class="btn btn-outline-primary mt-3 align-self-start" target="_blank" rel="noopener noreferrer">
              View Project
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</section> -->


    <!-- <section id=timeline>
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
            <a :href="`${project.purl}`"><img :src="`/images/projects/${project.image}`" alt="Graphic"></a>
            
          </div>
        </div>
      </div>
    </section> -->


    <div class="container" id=experience>
        <div ><h2 id="section-title">EXPERIENCE</h2>
          <div class="timeline-item" date-is='Aug 2022 - Jun 2023'>
            <h1>ASIAN MOBILE SOFTWARE</h1>
            <h4>
              Developed Android apps with Kotlin, utilizing Firebase, ML Kit, MediaPipe, OpenCV,... Focused on enhancing app functionality and optimizing performance.
            </h4>
          </div>
          <div class="timeline-item" date-is='Sept 2023 - Aug 2024'>
            <h1>GAMMAPP LTD</h1>
            <h4>
              Developed Android apps with Kotlin, working with Android Room, SQLite, API interaction, JSON, and custom views. Additionally, worked with Swift on iOS, using Realm, SQLite, and GRDB for database management.
            </h4>
          </div>
        
        </div>
          


    </div>
    <div class="container">
      <section id=skills>
        <h2 id="section-title">SKILLS</h2>
        <b-row>
          <b-col md="4">
            <div>
              <h2 class="skills-title">PROGRAMMING LANGUAGES</h2>
              <img  src="https://skillicons.dev/icons?i=kotlin,java,swift,python,cs,css,cpp,html,vue&theme=light&perline=6" />
              <!-- <img v-for="image in LANGUAGES" :key="image" :src="image"
                style="width: 70px; height: 70px; object-fit: cover;" /> -->
              <!-- <b-img thumbnail v-for="image in LANGUAGES" :key="image" :src="image" width="80" fluid alt="skills image" /> -->
            </div>

          </b-col>
          <b-col md="4">
            <div>
              <h2 class="skills-title">FRAMEWORKS &amp; TOOLS </h2>
              <img  src="https://skillicons.dev/icons?i=androidstudio,django,github,firebase,opencv,regex,vscode,postman,nuxtjs,figma&theme=light&perline=6" />
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
                  <li class="in"><a href="https://www.facebook.com/quangthang46/"><img src="/images/icon/facebook-icon-512x511-ircc9ves.png" class="icon-social" /></a></li>
                  <li class="fb"><a href="https://www.instagram.com/pqt46/"><img src="/images/icon/4138124.png" class="icon-social" /></a></li>
                  <li class="tw"><a href="https://github.com/thangpq46"><img src="/images/icon/github-512.webp" class="icon-social"/></a></li>
                  <li class="pin"><a href="https://www.tiktok.com/@qthang46"><img src="/images/icon/4138198.png" class="icon-social"/></a></li>
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
        { span: "span-2", c: "c-2", url: "/images/me/PXL_20240418_135809702.MP.jpg" },
        { span: "span-1", c: "c-2", url: "/images/me/PXL_20240420_112351861.jpg" },
        { span: "span-2", c: "c-4", url: "/images/me/PXL_20240420_072312313.jpg" },
        { span: "span-1", c: "c-4", url: "/images/me/PXL_20240601_125407730.jpg" },
        { span: "span-1", c: "c-5", url: "/images/me/c.jpg" },
        { span: "span-2", c: "c-2", url: "/images/me/PXL_20240420_073159792.jpg" },
        { span: "span-1", c: "c-5", url: "/images/me/PXL_20240713_132355640.jpg" },
        { span: "span-1", c: "c-5", url: "/images/me/PXL_20240419_063256839.MP.JPG" },
        { span: "span-1", c: "c-2", url: "/images/me/f.jpg" },
        { span: "span-1", c: "c-2", url: "/images/me/g.jpg" },
        { span: "span-3", c: "c-1", url: "/images/me/PXL_20240419_082620007.MP.jpg" },
        { span: "span-2", c: "c-2", url: "/images/me/IMG_5680.JPG" },
        { span: "span-2", c: "c-2", url: "/images/me/original_68b962c7-3f4d-49f3-892f-753f771045ca_PXL_20240713_140507700.jpg" },
        { span: "span-1", c: "c-4", url: "/images/me/E7D_1261~2.JPG" },
        { span: "span-1", c: "c-4", url: "/images/me/PXL_20240601_141334096.MP.jpg" },
        { span: "span-2", c: "c-1", url: "/images/me/PXL_20240428_141646989~3.jpg" },
        { span: "span-1", c: "c-2", url: "/images/me/original_91144d98-a737-40da-9d42-7693b9e30cef_PXL_20230908_110045522.jpg" },
        { span: "span-1", c: "c-2", url: "/images/me/PXL_20220916_224510370.jpg" },
        { span: "span-1", c: "c-4", url: "/images/me/PXL_20220917_223208400.MP.jpg" },
        { span: "span-1", c: "c-4", url: "/images/me/PXL_20231230_234309000~2.jpg" },
        { span: "span-1", c: "c-4", url: "/images/me/PXL_20230223_102453301.jpg" },
        { span: "span-1", c: "c-1", url: "/images/me/PXL_20230311_101713729.jpg" },
        { span: "span-1", c: "c-2", url: "/images/me/PXL_20240713_135101402.MP.jpg" },
      ],
      PROJECTS: [
      { step: "demo-card demo-card--step4", name: "PDF Reader", des: "PDF application with features including merging and splitting PDFs, converting images to PDF, editing PDF metadata,extracting text from PDFs, reordering pages, and exporting pages as images.", image: "pdf.png",purl:"https://drive.google.com/file/d/1-HYLcrP5SA-6RbPJD4vJXydmSX0TPA71/view?usp=sharing", technologies: ["ITextPdf", "Android Jetpack"] },   
        { step: "demo-card demo-card--step1", name: "Laptop Store", des: "Website with a backend server built using Django Rest Framework and a frontend created with NuxtJs.", image: "170959998-2c700593-52df-4ccf-ac58-def41a258212.png",purl:"https://github.com/thangpq46/TKVLTWCC" , technologies: ["Django REST framework", "Nuxtjs"," MySQL"," Simple JWT","Axios", "CorHeader","Coverage"]},
        { step: "demo-card demo-card--step2", name: "Qtor - Photor Editor", des: "Photo editor application with features including object removal, brightness and saturation adjustments, and adding stickers,timestamps, and text to images.", image: "249319500-65987689-8afa-490e-b6bb-dce76e6aa01c.png",purl:"https://github.com/thangpq46/Qtor" , technologies: ["Kotlin", "Custom View", "ML Kit", "OpenCV", "Firebase", "Android Jetpack"]},
        { step: "demo-card demo-card--step3", name: "Easy Notebook", des: "Simple Note application.", image: "376355443_1489736278466776_7192872528555101855_n.png",purl:"https://github.com/thangpq46/Fruit-Ninja", technologies: ["Android Jetpack", "Room"] },
           ],
    }
  }
}

</script>
