<template>
  <!-- site wrapper -->
<div class="site-wrapper">

	<div class="main-overlay"></div>

  <Header />

	<!-- section main content -->
	<section class="main-content">
		<div class="container-xl">

			<div class="row gy-4">

				<div class="col-lg-8">
					
					<!-- section header -->
					<div class="section-header">
						<h3 class="section-title text-uppercase">Latest Posts</h3>
					</div>

					<div class="padding-30 rounded bordered">

						<div class="row">
							
							<div class="col-md-12 col-sm-6" v-for="(front, i) in frontpage.data" :key="i">
								<!-- post -->
								<div class="post post-list clearfix">
									<div class="thumb rounded">
										<!-- <span class="post-format-sm">
											<i class="icon-picture"></i>
										</span> -->
										<NuxtLink :to="'' + front.slug">
											<div class="inner">
												<img :src='featuredImage+ front.featured_image' :alt="front.title" />
											</div>
										</NuxtLink>
									</div>
									<div class="details">
										<ul class="meta list-inline mb-3">
											<li class="list-inline-item text-capitalize"><a href="#">{{ front.username }}</a></li>
											<li class="list-inline-item"><NuxtLink :to="'/category/'+ front.category_slug ">{{ front.category }}</NuxtLink></li>
											<li class="list-inline-item">{{ front.created_at }}</li>
										</ul>
										<h5 class="post-title"><NuxtLink :to="'' + front.slug">{{ front.title }}</NuxtLink></h5>
										<p class="excerpt mb-0">{{ front.excerpt }}</p>
										<div class="post-bottom clearfix d-flex align-items-center">
											<div class="social-share me-auto">
												<button class="toggle-button icon-share"></button>
												<ul class="icons list-unstyled list-inline mb-0">
													<li class="list-inline-item"><a href="#"><i class="fab fa-facebook-f"></i></a></li>
													<li class="list-inline-item"><a href="#"><i class="fab fa-twitter"></i></a></li>
													<li class="list-inline-item"><a href="#"><i class="fab fa-linkedin-in"></i></a></li>
													<li class="list-inline-item"><a href="#"><i class="fab fa-pinterest"></i></a></li>
													<li class="list-inline-item"><a href="#"><i class="fab fa-telegram-plane"></i></a></li>
													<li class="list-inline-item"><a href="#"><i class="far fa-envelope"></i></a></li>
												</ul>
											</div>
											<div class="more-button float-end">
												<a href="blog-single.html"><span class="icon-options"></span></a>
											</div>
										</div>
									</div>
								</div>
							</div>
							
						</div
						>
						<!-- load more button -->
						<div class="text-center">
							<button class="btn btn-simple">Load More</button>
						</div>

					</div>

				</div>
				<Sidebar />

			</div>

		</div>
	</section>

	<!-- instagram feed -->
	<div class="instagram">
		<div class="container-xl">
			<!-- button -->
			<a href="#" class="btn btn-default btn-instagram">@Katen on Instagram</a>
			<!-- images -->
			<div class="instagram-feed d-flex flex-wrap">
				<div class="insta-item col-sm-2 col-6 col-md-2">
					<a href="#">
						<img src="images/insta/insta-1.jpg" alt="insta-title" />
					</a>
				</div>
				<div class="insta-item col-sm-2 col-6 col-md-2">
					<a href="#">
						<img src="images/insta/insta-2.jpg" alt="insta-title" />
					</a>
				</div>
				<div class="insta-item col-sm-2 col-6 col-md-2">
					<a href="#">
						<img src="images/insta/insta-3.jpg" alt="insta-title" />
					</a>
				</div>
				<div class="insta-item col-sm-2 col-6 col-md-2">
					<a href="#">
						<img src="images/insta/insta-4.jpg" alt="insta-title" />
					</a>
				</div>
				<div class="insta-item col-sm-2 col-6 col-md-2">
					<a href="#">
						<img src="images/insta/insta-5.jpg" alt="insta-title" />
					</a>
				</div>
				<div class="insta-item col-sm-2 col-6 col-md-2">
					<a href="#">
						<img src="images/insta/insta-6.jpg" alt="insta-title" />
					</a>
				</div>
			</div>
		</div>
	</div>

  <Footer />

</div><!-- end site wrapper -->

</template>

<script>
import Header from '@/components/Front/Header'
import Sidebar from '@/components/Front/Sidebar'
import Footer from '@/components/Front/Footer'
export default {
  // middleware: 'auth',
  name: 'MainSite',
  components:{
    Header,
    Sidebar,
    Footer,
  },
  data: () => ({
    frontpage: [],
	// featuredImage: '',
	// baseUrl: process.env.BASE_URL
  }),
//   mounted: function (){
// 	this.baseUrl = process.env.BASE_URL
//   },
  async asyncData({ $axios }) {
    const response = await $axios.get('/api/frontpage')
    return { frontpage: response.data.posts }
  },
  head(){
    return{
      title: 'Blog'
    }
  },
  method: {
	featuredImage(){
		if(!this.frontpage.featured_image) return "https://api.japachronicles.xyz/storage/normani-fair-listen-here-lyrics.jpg";
	  return this.$config.myPublicVariable + 'storage/'
	}
  }
	//   featuredImage: `${process.env.BASE_URL}` + 'storage/',
	
	//   return this.baseUrl + 'storage/'
	// },
  
}
</script>


<style scoped>
@import '~/assets/front/css/bootstrap.min.css';
@import '~/assets/front/css/all.min.css';
@import '~/assets/front/css/slick.css';
@import '~/assets/front/css/simple-line-icons.css';
@import '~/assets/front/css/style.css';
.spacer{
  height: 50px;
}
.section-header{
	padding-left: 10px;
    padding-top: 10px;
    padding-bottom: 10px;
   	border-radius: 10px;
    border: solid 1px #EBEBEB;
}
.section-title{
	text-align: center;
}
.author{
	border-radius: 9999px;
}
</style>
