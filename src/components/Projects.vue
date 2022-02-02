<template>
  <h1 class="heading"> My <span> Projects </span> </h1>
<div class="boxedd">
  
 
<div class="container">
    <div class="row">
        <div class="col-md-3 col-sm-6">
            <div class="our-teams">
                <div class="pic">
                    <img src="../assets/projA.jpg">
                </div>
                <div class="teams-content">
                    <h3 class="title">Portfolio</h3>
                    <span class="post">Html Css</span>
                    <ul class="social">
                        <li><a href="https://github.com/Na-aim/Portfolio_0ne-main-main" target="_blank" class="fab fa-github" ></a></li>
                        <li><a href="https://fervent-ramanujan-3e98df.netlify.app" target="_blank" class="fas fa-eye"></a></li>
                    </ul>
                </div>
            </div>
        </div>
 
        <div class="col-md-3 col-sm-6">
            <div class="our-teams">
                <div class="pic">
                    <img src="../assets/projB.jpg">
                </div>
                <div class="teams-content">
                    <h3 class="title">Point of Sale</h3>
                    <span class="post">HTML CSS JS</span>
                    <ul class="social">
                         <li><a href="https://github.com/Na-aim/naaims_P.O.S" target="_blank" class="fab fa-github"></a></li>
                        <li><a href="https://na-aim-pos.netlify.app" target="_blank" class="fas fa-eye"></a></li>
                    </ul>
                </div>
            </div>
        </div>
      
       <div class="col-md-3 col-sm-6">
            <div class="our-teams">
                <div class="pic">
                    <img src="../assets/projC.jpg">
                </div>
                <div class="teams-content">
                    <h3 class="title">Pokeidex</h3>
                    <span class="post">HTML CS JS</span>
                    <ul class="social">
                         <li><a href="https://github.com/Na-aim/Pokedex" target="_blank" class="fab fa-github"></a></li>
                        <li><a href="#http://127.0.0.1:5500/index.html" target="_blank" class="fas fa-eye"></a></li>
                    </ul>
                </div>
            </div>
        </div>
      
       <div class="col-md-3 col-sm-6">
            <div class="our-teams">
                <div class="pic">
                    <img src="../assets/projD.jpg">
                </div>
                <div class="teams-content">
                    <h3 class="title">Temperature Convertor</h3>
                    <span class="post">HTML CSS JS</span>
                    <ul class="social">
                        <li><a href="https://github.com/Na-aim/temp-cal" target="_blank" class="fab fa-github"></a></li>
                        <li><a href="#" target="_blank" class="fas fa-eye"></a></li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</div>
</div>

</template>

<script>
export default {

}
</script>

<style scoped>

 .boxedd{
    padding-top: 190px;
    padding-bottom:200px ;
    padding-left: 10rem;
    padding-right: 10rem;
}

.our-teams .pic{
    border-top: 5px solid var(--main-color);
    border-bottom: 5px solid var(--main-color);
    border-radius: 50% 50% 50% 0;
    overflow: hidden;
    transition: all 0.5s ease 0s;
}
.our-teams:hover .pic{
    border-top-color: #000000;
    border-bottom-color: #000000;
    border-radius: 50% 0;
}
.our-teams .pic img{
    width: 100%;
    height: auto;
    transition: all 0.5s ease 0s;
}
.our-teams .team-content{ padding: 20px 0; }
.our-teams .title{
    font-size: 22px;
    font-weight: 700;
    color: var(--main-color);
    text-transform: uppercase;
    margin: 0 0 5px 0;
}
.our-teams .post{
    display: block;
    font-size: 17px;
    color: #000000;
    margin-bottom: 10px;
}
.our-teams .social{
    list-style: none;
    padding: 0;
    margin: 0;
}
.our-teams .social li{ display: inline-block; }
.our-teams .social li a{
    display: block;
    width: 35px;
    height: 35px;
    line-height: 35px;
    border-radius: 50%;
    border: 1px solid black;
    background: #fff;
    font-size: 17px;
    color: #000000;
    text-align: center;
    transition: all 0.5s ease 0s;
}
.our-teams:hover .social li a{
    background: var(--main-color);
    color: #fff;
}
@media only screen and (max-width: 990px){
    .our-team{ margin-bottom: 30px; }
}

</style>