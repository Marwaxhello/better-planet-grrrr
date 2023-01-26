<template>
  <div id="landing-page">
    <img id="top-nav-design" src="~/assets/design.svg" alt="design">  
    <div id="landing-page-inner">
      <h1 class="animate-charcter">50K</h1>
      <h3>for a better planet</h3>
      <CustomButton xl="true" label="apply now" />
      <p class="body-1">Deadline feb 13, 2023</p>
      <p class="body-1">
        We believe that climate-tech startups have the power to make a
        significant positive social impact on a large scale. We want to help
        these startups get on their feet, faster. That’s why we’re investing
        €50.000 in a startup fund, providing promising pioneers with the tools
        they need to push their mission further.
      </p>
      <img  src="~/assets/images/case-1.png" alt="case-1" />

      <HeaderBlock text="Who’s behind this?" />

      <p class="body-1">
        GRRR is a creative digital agency for Meaningful Matters. We strive to
        make the world cleaner, fairer and more colourful, and have been working
        towards this mission for over 20 years now. We were the first Dutch
        digital creative agency with a B-Corp certificate, and our focus on
        impact strategy, inclusive design and ethical tech has been recognised
        with 33 international awards and nominations. Seeing our work realised
        in the success of companies like The Ocean Cleanup (with xx result),
        Fastned (with xx result) and SkyNRG (with xx result) is what keeps us
        going.
      </p>

      <img v-vue-aos="{animationClass:'fadeLeft animated'}" src="~/assets/images/ocean-clean-up.png" alt="Clean-up" />


      <HeaderBlock text="WHAT’S THE FUND?" />

      <p class="body-1">
        The startup fund was born from our mission: helping all organisations
        become more meaningful, regardless of where they’re at on their impact
        journey. We took this one step further.
      </p>

      <HeaderBlock text="GOOD DESIGN FOR A BETTER PLANET?" />

      <p class="body-1">
        Design goes beyond what looks nice. It’s your brand's personality; how
        it looks, talks, reacts and interacts with people. Good design can make
        a brand easier to understand, to use, more memorable and more
        accessible. It gets your mission across and your message out there.
        That’s why we're funding climate-tech startups; we want to give them the
        power to stand out, to make even more impact, to be even more
        successful, and ultimately, to build towards a more sustainable future.
      </p>

      <HeaderBlock text="HOW IT WORKS" />

      <p class="body-1">
        You’ll enter the brand-pressure cooker, a fast-paced brand immersion,
        together with our team of brand identity experts. We’ll guide you
        through the process of (re)defining your mission and messaging, followed
        by visualising your brand, over the following four phases:
      </p>


      <ul class="body-1">
        <li>Phase Two: Visual Identity</li>
        <li>Phase Three: Communication Tools (pitch deck, storyline, tone of voice guidelines)  </li>
        <li>Phase Four: One page Website </li>
      </ul>

      <p class="body-1" >At the end of the process you’ll be armed with a clear</p>

      <HeaderBlock text="WHO’S ELIGIBLE?" />
      <p class="body-1">
        Applications are open to climate-tech companies who are on the early
        stage of their startup journey. Applicants will be assessed based on the
        questions answered in the application form, but must also be able to:
      </p>



      <ul class="body-1">
        <li>Provide input and feedback </li>
        <li>Be available to invest time in the process  </li>
        <li>Be agile and willing to work under high pressure </li>
      </ul>

      <p class="body-1">
                We’d like to ensure the fund applicant is chosen fairly and accurately.
        GRRR will form a small, confidential panel to review the applications.
        If there is no clear candidate, GRRR reserves the right to either extend
        the deadline or postpone the fund until there is a suitable applicant.
        All work submitted will remain confidential and not disclosed to third
        parties.
      </p>

      <h3 class="center-text">Partners</h3>
      <div class="partners">
        <img src="~/assets/images/b-lap-europe.webp" alt="b lab europe">
        <img src="~/assets/images/change-inc.png" alt="change inc">
        <img src="~/assets/images/logo.png" alt="logo">
      </div>
      
      <div class="deadline-section">
        <CustomButton  xl="true" label="apply now"></CustomButton>
        <p class="body-1">Deadline feb 13, 2023</p>
      </div>

      <p class="body-1 center-text">
        This is a project by GRRR - creative agency for meaningful matters,
        based in Amsterdam.
      </p>

    </div>
    <img id="bottom-nav-design" src="~/assets/design.svg" alt="design">  

  </div>
</template>

<script>
import CustomButton from '~/components/CustomButton.vue'
import HeaderBlock from '~/components/HeaderBlock.vue'

export default {
  name: 'IndexPage',
  components: { HeaderBlock },
}
</script>

<style lang="scss">

#landing-page {
  width: 100%;
  display: flex;
  position: relative;
  justify-content: center;
  background: rgb(81,69,255);
  background: radial-gradient(circle, rgba(81,69,255,1) 5%, rgba(255,237,220,1) 76%);
}

#landing-page h1{
  margin-top: 7rem;
  color: $primary-green;


                @media only screen and (max-width: $tablet) {
                        color:$primary-blue;
                    }
}

#top-nav-design{
  // width: 100vw;
  height: 50rem;
  position: absolute;
  top: 0;
  right: 0;
  left: 0;
  z-index: 0;
}

#bottom-nav-design{
  width: 100vw;
  position: absolute;
  bottom: -8rem;
  right: 0;
  left: 0;
  z-index: 0;
  transform: rotate(180deg)
}

              @media only screen and (max-width: $tablet) {
       #bottom-nav-design, #top-nav-design{
        display: none;
       }
      }


img {
  margin-bottom: 3rem;
    border-radius: 4px;

              @media only screen and (max-width: $tablet) {
        width: 100%;
      }
}

.partners{
  display: flex;
  justify-content: center;
  margin-bottom: 3rem;

          @media only screen and (max-width: $tablet) {
        flex-direction: column;
      }

  img {
    height: 8rem;
    object-fit: contain;
    margin-right: 2rem;

           @media only screen and (max-width: $tablet) {
        width: 100%;
      }
  }
}

.deadline-section{
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  flex-grow: 0;
}

 
#landing-page-inner {
  width: 860px;
  z-index: 1;
  // border: 1px solid blue;

       @media only screen and (max-width: $tablet) {
        width: 100%;
           padding: 0 2.875rem;
      }
}

@keyframes anim {
  from {
    text-shadow: 0 0 10px transparent;
  }
  to {
    text-shadow: 0 28px 50px rgba(0, 0, 0, 0.8);
  }
}



</style>
