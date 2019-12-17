<template>
  <main id="home">
    <section class="page-header">
      <div class="col-lg-6 col-md-12 col-sm-24 d-flex">
        <div class="small-orange-cirle"></div>
        <div class="image-container">
          <img src="@/assets/img/Mask Group.png" alt="">
        </div>
        <div class="user-details">
          <h2 class="font-weight-bold">Sarah Abra</h2>
          <p>Ui&amp;UX Designer</p>
          <button class="btn btn-sm tap">Tap to chat</button>
          <div class="user-social-icons">
            <i class="fab fa-behance"></i>
            <i class="fab fa-dribbble"></i>
            <i class="fab fa-instagram"></i>
            <i class="fab fa-linkedin-in"></i>
            <i class="fab fa-facebook-f"></i>
          </div>
        </div>
      </div>
      <div class="col-lg-6 col-md-12 col-sm-24 user-rates">
        <div class="d-flex justify-content-between interviews">
          <h4>Your Interviews :</h4>
          <img src="@/assets/img/image 2.png" alt="">
        </div>
        <div class="user-rates__all">
          <div class="text-center">
            <h5>10$</h5>
            <p>Hourly rate</p>
          </div>
          <div class="text-center">
            <h5>35 hours</h5>
            <p>Weekly Availability</p>
          </div>
          <div>
            <button class="btn btn-sm tap">Hire me</button>
          </div>
        </div>
      </div>
    </section>

    <section class="about-user">
      <div class="about-user__tabs" id="tabs">
        <div>
          <a 
            id="first-tab"
            :class="{ active: isActive('portfolio') }"
            data-toggle="tab"
            role="tab"
            aria-controls="first"
            aria-selected="true"
            @click.prevent="setActive('portfolio')">
            
            <h5 :class="{ active: isActive('portfolio') }">Portfolio</h5>
          </a>
      </div>
      <div>
        <a 
          id="second-tab"
          data-toggle="tab"
          role="tab"
          aria-controls="second"
          aria-selected="true"
          @click.prevent="setActive('work')">

          <h5 :class="{ active: isActive('work') }">Work</h5>
        </a>
      </div>
      <div>
        <a 
          id="third-tab"
          data-toggle="tab"
          role="tab"
          aria-controls="third"
          aria-selected="true"
          @click.prevent="setActive('education')">

          <h5 :class="{ active: isActive('education') }">Education</h5>
        </a>
      </div>
      </div>

      <div id="myTabContent" class="tab-content">
        <div
          id="portfolio"
          class="tab-pane"
          role="tabpanel"
          aria-labelledby="first-tab"
          :class="{ 'active show': isActive('portfolio') }">
          <div class="tab-content__one">
            <h5>Programing Language</h5>
            <h5>Frameworks / Databases</h5>
            <h5>Design Skills</h5>
            <h5>Software</h5>
          </div>
          <div class="d-flex">
            <div class="col-lg-6 col-md-12 col-sm-12">
              <img src="@/assets/img/Mask Group.svg" alt="" class="w-100">
            </div>
            <div class="col-lg-6 col-md-12 col-sm-12 mask">
              <img src="@/assets/img/Mask Groupp.png" alt="" class="w-100">
            </div>
          </div>
        </div>

        <div
          id="work"
          class="tab-pane"
          role="tabpanel"
          aria-labelledby="second-tab"
          :class="{ 'active show': isActive('work') }">

          <div class="tab-content__one">
            <h5>Programing Language</h5>
            <h5>Frameworks / Databases</h5>
            <h5>Design Skills</h5>
            <h5>Software</h5>
          </div>

          <div class="work-details">
            <div class="work-details__head">
              <div class="black-circle"></div>
              <h4>Senior UI&amp;UX Designer</h4>
            </div>
            <p class="pl-4">May 2018 - Jul 2018</p>
            <p class="pl-4 work-details__more">Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum.</p>

            <div class="work-details__head">
              <div class="black-circle"></div>
              <h4>Graphic designer</h4>
            </div>
            <p class="pl-4">May 2018 - Jul 2018</p>
            <p class="pl-4 work-details__more">Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore</p>

          </div>
        </div>

        <div
          id="education"
          class="tab-pane"
          role="tabpanel"
          aria-labelledby="third-tab"
          :class="{ 'active show': isActive('education') }">

          <div class="tab-content__one">
            <h5>Programing Language</h5>
            <h5>Frameworks / Databases</h5>
            <h5>Design Skills</h5>
            <h5>Software</h5>
          </div>
          <div class="work-details">
            <div class="work-details__head">
              <div class="black-circle"></div>
              <h4>Oxford university</h4>
            </div>
            <p class="pl-4">May 2018 - Jul 2018</p>
            <p class="pl-4 work-details__more">Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum.</p>

            <div class="work-details__head">
              <div class="black-circle"></div>
              <h4>Udemy</h4>
            </div>
            <p class="pl-4">May 2018 - Jul 2018</p>
            <p class="pl-4 work-details__more">Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore</p>

          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  name: 'home',
  data() {
    return {
      activeItem: 'portfolio',
    }
  },
  methods: {
    isActive (menuItem) {
      return this.activeItem === menuItem;
    },
    setActive (menuItem) {
      this.activeItem = menuItem;
    },
  }
  
}
</script>

<style scoped>

</style>