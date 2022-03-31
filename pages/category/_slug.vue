<template>
  <div class="site-wrapper">
    <div class="main-overlay"></div>

    <Header />
    <section class="main-content">
      <div class="container-xl">

			<div class="row gy-4">

				<div class="col-lg-8">

          <div class="row gy-4">
              <div class="col-sm-6">
                  <!-- post -->
                  <div class="post post-grid rounded bordered">
                      <div class="thumb top-rounded">
                          <a href="category.html" class="category-badge position-absolute">Lifestyle</a>
                          <span class="post-format">
                              <i class="icon-picture"></i>
                          </span>
                          <a href="blog-single.html">
                              <div class="inner">
                                  <img src="images/posts/post-md-1.jpg" alt="post-title" />
                              </div>
                          </a>
                      </div>
                      <div class="details">
                          <ul class="meta list-inline mb-0">
                              <li class="list-inline-item"><a href="#"><img src="images/other/author-sm.png" class="author" alt="author"/>Katen Doe</a></li>
                              <li class="list-inline-item">29 March 2021</li>
                          </ul>
                          <h5 class="post-title mb-3 mt-3"><a href="blog-single.html">How To Become Better With Building In 1 Month</a></h5>
                          <p class="excerpt mb-0">I am so happy, my dear friend, so absorbed in the exquisite sense of mere tranquil existence.</p>
                      </div>
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

              <div class="col-sm-6">
                  <!-- post -->
                  <div class="post post-grid rounded bordered">
                      <div class="thumb top-rounded">
                          <a href="category.html" class="category-badge position-absolute">Inspiration</a>
                          <a href="blog-single.html">
                              <div class="inner">
                                  <img src="images/posts/post-md-2.jpg" alt="post-title" />
                              </div>
                          </a>
                      </div>
                      <div class="details">
                          <ul class="meta list-inline mb-0">
                              <li class="list-inline-item"><a href="#"><img src="images/other/author-sm.png" class="author" alt="author"/>Katen Doe</a></li>
                              <li class="list-inline-item">29 March 2021</li>
                          </ul>
                          <h5 class="post-title mb-3 mt-3"><a href="blog-single.html">Most Important Thing You Need To Know About Swim</a></h5>
                          <p class="excerpt mb-0">I am so happy, my dear friend, so absorbed in the exquisite sense of mere tranquil existence.</p>
                      </div>
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

					<nav>
						<ul class="pagination justify-content-center">
							<li class="page-item active" aria-current="page">
								<span class="page-link">1</span>
							</li>
							<li class="page-item"><a class="page-link" href="#">2</a></li>
							<li class="page-item"><a class="page-link" href="#">3</a></li>
						</ul>
					</nav>

				</div>
			

					<Sidebar />


			</div>

		</div>
    </section>
  </div>
</template>

<script>
import Header from '@/components/Front/Header'
import Sidebar from '@/components/Front/Sidebar'
import Footer from '@/components/Front/Footer'
import AuthorCard from '@/components/Front/AuthorCard'
export default {
  components:{
    Header,
    Sidebar,
    Footer,
    AuthorCard,
  },
  data: () => ({
    post:[]
  }),
  // async fetch(){
  //   await this.$axios.get('/api/frontpage/'+this.$route.params.slug)
  //  .then(response => {
  //    this.post = response.data
  //  })
  //   .catch(error => {
  //     ({
  //       message: 'Error',
  //       statusCode: 404,
  //       status: 404,
  //       statusText: 'Not Found',
  //     })
  //   })
  // },
}
</script>

<style>
@import '~/static/front/css/bootstrap.min.css';
@import '~/static/front/css/all.min.css';
@import '~/static/front/css/slick.css';
@import '~/static/front/css/simple-line-icons.css';
@import '~/static/front/css/style.css';
 .spacer{
  height: 50px;
} 
</style>