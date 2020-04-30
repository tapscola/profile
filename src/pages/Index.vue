<template>
  <Layout>
    <fork-github :githubUrl="profile.githubUrl" v-if="profile.githubUrl" />
    <Intro :socials="profile.socials" :personal="profile.personal"/>
    <div class="layout">
      <overview
        :socials="profile.socials"
        :personal="profile.personal"
        :coffeeDonateUrl="profile.buy_me_coffee_url"/>
    </div>
  </Layout>
</template>

<script>
import Intro from '~/components/introduction/Intro.vue'
import profile from '~/data/profile.json'
import ForkGithub from '~/components/common/ForkGithub.vue'

export default {
  components: {
    Intro,
    ForkGithub
  },
  data: () => ({
    profile
  }),
  metaInfo: {
    title: 'Tapiwa Musasa Profile'
  }
}
</script>

<style>
.layout {
  max-width: 760px;
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
}
</style>
