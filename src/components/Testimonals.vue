<template>  
 
  <div class="container5">
      <h1 class="heading"> My <span> Testimonals</span> </h1>
    <div class="row">
        <div class="col-md-4 col-sm-12"  v-for="testimonial of testimonials" :key="testimonial.id" >
            <div class=" our-team">
                <div class="pic">
                    <div class="layer-1">
                        <div class="layer-2">
                            <div class="layer-3">
                                <img :src="testimonial.img" alt="">
                                <!-- <img src="../assets/Alex.jpg" alt=""> -->
                                <div class="social">
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="team-info">
                        <h3 class="title">{{testimonial.name}}</h3>
                            <!-- Alex Sexwale -->
                        <span class="post">{{testimonial.relation}}</span>
                            <!-- Leacturer -->
                    </div>
                </div>
                <p class="description">
                    {{testimonial.quote}}
                    <!-- Na-aim thrives in doing better than the previous day.He has a strong determination to do anything.He makes decisions with confidence.. -->
                </p>
            </div>
        </div>
    </div>
</div>
</template>



<script>
export default {
   data(){
            return {
        testimonials:[]
            }
        },

        
        mounted(){
            fetch('  https://express-backend1.herokuapp.com/testimonal')
            .then(res => res.json())
            .then(data => this.testimonials = data)
            .catch(err => console.log(err.message))
        }
}
</script>

<style scoped>
.container5{
    padding-top: 100px;
    padding-left: 10rem;
    padding-right: 10rem;
}
.demo{ background: #f8f8f8; }
.our-team{
    overflow: hidden;
    position: relative;
    width: 300px;
    height: 500px;
    display:flex;
    justify-content: center;
    flex-wrap: wrap;
}
.our-team .pic{
    padding-bottom: 20px;
    margin-bottom: 30px;
}
.our-team .layer-1{
    width: 200%;
    overflow: hidden;
    transform: rotate(10deg) translate(-13%, 13%);
}
.our-team .layer-2{
    background: #fff;
    overflow: hidden;
    transform: rotate(-16deg) translate(-9%, -13%);
}
.our-team .layer-3{
    width: 51%;
    margin: 0 auto;
    transform: rotate(6deg) translateY(5%);
}
.our-team img{
    width: 100%;
    height: 350px;
    object-fit: cover;
    flex-wrap: wrap;
}
.our-team .social{
    width: 50%;
    height: 150%;
    background: linear-gradient(to right, rgba(244, 205, 3, 0), var(--main-color));
    position: absolute;
    bottom: 0;
    right: 0;
    transform: translateX(100%);
    transition: all 0.3s ease-out 0s;
}

.our-team:hover .social{
    transform: translateX(0px);
}
.our-team .social-icon{
    list-style: none;
    padding: 0;
    margin: 0;
    width: 30px;
    position: absolute;
    bottom: 95px;
    right: 15px;
}
.our-team .social-icon li a{
    display: inline-block;
    width: 30px;
    height: 30px;
    line-height: 30px;
    background: #fff;
    border-radius: 50%;
    font-size: 13px;
    color: #000;
    text-align: center;
    margin: 4px 0;
    transform: scale(0);
    transition: all 0.2s ease-out 0.4s;
}
.our-team:hover .social-icon li a{
    transform: scale(1);
}
.our-team .social-icon li a.fa-facebook:hover{ color: var(--main-color); }
.our-team .social-icon li a.fa-google-plus:hover{ color: #db4437; }
.our-team .social-icon li a.fa-twitter:hover{ color: var(--main-color); }
.our-team .team-info{
    padding: 15px 15px 20px;
    margin: 25px;
    background: var(--main-color);
    border-radius: 3px;
    text-align: center;
    position: absolute;
    bottom: 100px;
    left: 0;
    right: 0;
    transition: all 0.2s ease-out 0s;
}
.our-team:hover .team-info{
    background: #fff;
}
.our-team .title{
    font-size: 18px;
    color: #000;
    margin: 0;
}
.our-team .post{
    display: block;
    font-size: 14px;
    font-style: italic;
    color: #000000;
    margin-top: 5px;
}
.description{
    margin-top: -20px;
}

.our-team .description{
    padding: 0 20px;
    font-size: 14px;
    color: #000000;
    text-align: center;
}
@media only screen and (max-width: 990px){
    .our-team{ margin-bottom: 20px; }
     
}
@media only screen and (max-width: 767px){
    .our-team .social-icon{ right: 25px; }
    .our-team .team-info{ bottom: 30px; }
   
}
@media only screen and (max-width: 767px){
    .our-team .team-info{ bottom: 65px; }
}
</style>