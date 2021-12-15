<template>

<div class="container-fluid">
  <div class="row justify-content-center pt-4 pb-5 search-container">
    <div class="col-sm-12">
      <img class="home-logo" src="/images/ignition-logo.svg" alt="">
      <h1 class="kb-title">Hi, how can we help you?</h1>
      <p class="kb-description">Enter a search term to find all related articles</p>
    </div>
    <div class="col-sm-12" id="search-home">
      <AlgoliaSearchBox
        v-if="isAlgoliaSearch"
        :options="algolia"
      />
      <SearchBox v-else-if="$site.themeConfig.search !== false && $page.frontmatter.search !== false"/>
    </div>
  </div>
  <div class="row justify-content-center pt-2">
    <div class="col-sm-12">
      <router-link to="/guides/ignition/" class="guide-link">
      <p class="kb-btn"><span>Browse all articles</span></p>
      </router-link>
    </div>
  </div>
</div>

</template>

<script>
import AlgoliaSearchBox from '@AlgoliaSearchBox'
import SearchBox from '@SearchBox'

export default {
  components: { SearchBox, AlgoliaSearchBox },

  data () {
    return {
    }
  },
  mounted () {
  },
  computed: {
    algolia () {
      return this.$themeLocaleConfig.algolia || this.$site.themeConfig.algolia || {}
    },
    isAlgoliaSearch () {
      return this.algolia && this.algolia.apiKey && this.algolia.indexName
    }
  }
}
</script>

<style scoped>

.content__default {
  min-width: 100%!important;
  padding-top: 0!important;
  margin: 0 auto;
}

h1:hover, h2:hover, h3:hover, h4:hover, h5:hover, h6:hover{
  transform: none;
}

.home-logo{
  position: relative;
  margin: 60px auto;
  display: block;
  width: 300px;
}

.search-container{
  color: #282828;
  background-size: cover;
  background-position: left;
}

.kb-title,
.kb-description{
  text-align: center;
}

.kb-btn{
  text-align: center;
  color: #282828;
  font-weight: 300;
  font-size: 16px;
}

.kb-btn span{
  padding: 10px 15px;
  border: 1px solid #cfd4db;
  border-radius: 0.3em;
  transition: 0.3s;
}

.kb-btn span:hover{
  border: 1px solid #D04F34;
  background-color: #D04F34;
  color: #fff;
  transition: 0.3s;
}



</style>
