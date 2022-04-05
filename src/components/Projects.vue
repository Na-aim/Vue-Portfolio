<template>

<div class="boxedx"> <h1 class="heading"> My <span> Projects </span> </h1></div>
 
<div  class="boxedd">

<div class="container">
    <div class="row">
        <div class="col-md-4 col-sm-6"  v-for="project in projects" :key="project.id" >
            <div class="our-team">
                <div class="team-image">
                    <img :src="project.img">
                    <ul class="social">
                        <li><a :href="project.github" target="_blank" class="fab fa-github" ></a></li>
                        <li><a :href="project.live" target="_blank" class="fas fa-eye"></a></li>
                    </ul>
                </div>
                <div class="team-content">
                    <h3 class="title">{{project.title}}</h3>
                    <p class="description">{{project.post}}.</p>
                </div>
            </div>
        </div>
    </div>
</div>
</div>


</template>

<script>


export default {
        data() {
            return {
                projects:[]
            }
        },
        mounted() {
            fetch('https://express-backend1.herokuapp.com/projects')
            .then(response => response.json())
            .then(data => this.projects = data)
            .catch(error => console.log(error.message))
        }
}
</script>

<style scoped>

.boxedx{
    padding-top: 100px;
    
}
 .boxedd{
    padding-top: 100px;
    padding-bottom:200px ;
    padding-left: 10rem;
    padding-right: 10rem;
    
}

.our-team{
    text-align: center;
}
.our-team .team-image{
    width: 80%;
    height: 80%;
    border-radius: 50%;
    border: 5px solid #d7d7d7;
    position: relative;
    margin: 0 auto;
    transition: all 0.5s ease 0s;
}
.our-team:hover .team-image{
    border-color: #db4437;
}
.our-team .team-image img{
    width: 100%;
    height: auto;
    border-radius: 50%;
}
.our-team .social{
    margin: 0;
    padding: 0;
    list-style: none;
    width: 100%;
    position: absolute;
    top: 45%;
    opacity: 0;
    transform: scale(0);
    transition: all 0.5s ease 0s;
}
.our-team:hover .social{
    opacity: 1;
    transform: scale(1);
    animation: 0.5s ease 0s normal 1 bounce;
}
.our-team .social li{
    display: inline-block;
    border-radius: 50%;
}
.our-team .social li:first-child{
    margin-left: -30px;
    float: left;
}
.our-team .social li:last-child{
    margin-right: -30px;
    float: right;
}
.our-team .social li a{
    display: block;
    width: 50px;
    height: 50px;
    line-height: 47px;
    border-radius: 50%;
    background-color: #fff;
    font-size: 25px;
    color: #222;
    border: 3px solid #db4437;
}
.our-team .team-content{
    padding: 10px 50px;
}
.our-team .title{
    font-size: 24px;
    color: #222;
    margin: 0 0 10px 0;
}
.our-team .description{
    font-size: 14px;
    color: #555;
    line-height: 25px;
    margin: 0;
}
@keyframes bounce{
    0%{
        opacity:0;
        -webkit-transform:scale(.3);
        transform:scale(.3)
    }
    50%{
        opacity:1;
         -webkit-transform:scale(1.05);
         transform:scale(1.05)
    }
    70%{
        -webkit-transform:scale(.9);
        transform:scale(.9)
    }
    100%{
        opacity:1;
        -webkit-transform:scale(1);
        transform:scale(1)
    }
}
@media screen and (max-width: 990px){
    .our-team{ margin-bottom: 20px; }
}

</style>