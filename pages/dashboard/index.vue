<template>
  <div>
    <LeftBar />
    <div class="relative md:ml-64 bg-blueGray-50">
      <TopBar />
      <div class="relative bg-pink-600 md:pt-32 pb-32 pt-12">
        <div class="px-4 md:px-10 mx-auto w-full">
          <div>
            <CenterContent />
          </div>
        </div>
      </div>
      <FrontPage />
    </div>
  </div>
</template>

<script>
import LeftBar from '@/components/Dashboard/LeftBar'
import TopBar from '@/components/Dashboard/TopBar'
import CenterContent from '@/components/Dashboard/CenterContent'
import FrontPage from '@/components/Dashboard/FrontPage'
export default {
  name: 'IndexPage',
  components:{
    LeftBar,
    TopBar,
    CenterContent,
    FrontPage
  }
}
</script>