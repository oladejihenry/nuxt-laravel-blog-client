<template>
   <div>
    <LeftBar />
    <div class="relative md:ml-64 bg-blueGray-50">
      <TopBar />
      <div class="relative bg-pink-600 md:pt-32 pb-32 pt-12">
      </div>
    </div>
  </div>
</template>

<script>
import LeftBar from '@/components/Dashboard/LeftBar'
import TopBar from '@/components/Dashboard/TopBar'
export default {
  name: 'IndexPage',
  components:{
    LeftBar,
    TopBar
  },
  head(){
    return{
      title: 'Settings'
    }
  },
}
</script>