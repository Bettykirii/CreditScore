Skip to content
Search or jump to…

Pull requests
Issues
Marketplace
Explore
 
@Bettykirii 
maeganwilson
/
vue-nav
1
11
16
Code
Issues
Pull requests
Actions
Projects
Wiki
Security
Insights
vue-nav/front-end/src/components/Navigation.vue
@maeganwilson
maeganwilson All done
Latest commit 0f8da93 on Dec 11, 2017
 History
 1 contributor
48 lines (46 sloc)  761 Bytes
  
<template>
  <div>
    <h2>Nav Bar</h2>
    <nav>
      <router-link class="spacing" v-for="routes in links" 
      v-bind:key="routes.id"
      :to="`${routes.page}`">{{routes.text}}</router-link>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'Navigation',
  data() {
    return {
      links: [
        {
          id: 0,
          text: 'Hello World',
          page:'/HelloWorld'
        },
        {
          id: 1,
          text: 'Home',
          page:'/Home'
        },
        {
          id: 2,
          text: 'About',
          page:'/About'
        },
        {
          id: 3,
          text: 'Contact',
          page:'/Contact'
        }
      ]
    }
  }
}
</script>
<style>
.spacing {
  margin-right: 10px;
}
</style>

