<template>
  <div id='sponsors-area' class='section section-padding-extra section-bg'>
    <div class='container'>
      <div class='row'>
          <div class='col-md-6 col-md-offset-3 text-center'>
            <div class='section-heading'>
              <h2 class='section-title'>Sponsors</h2>
              <p class='section-subtitle'>Nuestros patrocinadores</p>
              <router-link to="sponsor" target='_blank' class='linkSponsor'>Quieres ser patrocinador?</router-link>
            </div>
          </div>
      </div>
      <div class='row'>
        <div class='fun-facts'>
          <div class='col-md-4 text-center' v-for='(sponsor, key) in sponsors' :key="key">
            <div class='fun-fact'>
              <a v-bind:href='sponsor.website'>
                <div class='reviewer-mock'><img v-bind:src='sponsor.logo' alt='sponsor.name'></div>
                <p class='fact-name'>{{ sponsor.name }}</p>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  data () {
    return {
      sponsors: {
        HUGE: {
          name: 'HUGE',
          logo:
            'https://en.gravatar.com/userimage/46333208/108cf2fa50119a1781427d15fe29f64b.jpg?size=200',
          website: 'https://www.hugeinc.com'
        },
        RutaN: {
          name: 'RutaN',
          logo:
            'https://pbs.twimg.com/profile_images/948573975847849985/_It5tvFS_200x200.jpg',
          website: 'https://www.rutanmedellin.org'
        },
        TeamInternational: {
          name: 'TeamInternational',
          logo:
            'https://pbs.twimg.com/profile_images/963875088591409152/krlRSDkp_200x200.jpg',
          website: 'https://teaminternational.com'
        }
      }
    }
  }
}
</script>

<style scoped>
.linkSponsor {
  color: #fff;
  font-weight: bold;
}
</style>
