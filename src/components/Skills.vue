<template>

<div class="container3">
<h1 class="heading"> <span> my </span> skills </h1>
</div>
 <div class="container">
    <div class="row">
        <div class="col-md-6">
            <div class="progress pink">
                <h3 class="progress-title">HTML</h3>
                <div class="progress-value">95%</div>
                <div class="progress-bar" style="width:95%; background:linear-gradient(to right,var(--main-color),#ff4a98);"></div>
            </div>
            <div class="progress green">
                <h3 class="progress-title">CSS</h3>
                <div class="progress-value">90%</div>
                <div class="progress-bar" style="width: 90%;  background:linear-gradient(to right,var(--main-color),#ff4a98);"></div>
            </div>
            <div class="progress blue">
                <h3 class="progress-title">Java Script</h3>
                <div class="progress-value">60%</div>
                <div class="progress-bar" style="width: 60%;  background:linear-gradient(to right,var(--main-color),#ff4a98);"></div>
            </div>
            <div class="progress orange">
                <h3 class="progress-title">Database</h3>
                <div class="progress-value">80%</div>
                <div class="progress-bar" style="width: 80%;  background:linear-gradient(to right,var(--main-color),#ff4a98);"></div>
            </div>
            <div class="progress red">
                <h3 class="progress-title">Vue Cli</h3>
                <div class="progress-value">85%</div>
                <div class="progress-bar" style="width: 85%;  background:linear-gradient(to right,var(--main-color),#ff4a98);"></div>
            </div>
            <div class="progress black">
                <h3 class="progress-title">Bootstrap</h3>
                <div class="progress-value">89%</div>
                <div class="progress-bar" style="width: 89%;  background:linear-gradient(to right,var(--main-color),#ff4a98);"></div>
            </div>
        </div>
    </div>
</div>

</template>

<script>
export default {
    
}
</script>

<style>
.container3{
    padding-top: 100px;
    padding-left: 10rem;
    padding-right: 10rem;
}
.progress{
    height: 20px;
    background: #fff;
    border-radius: 15px 0 0 15px;
    box-shadow: none;
    margin: 20px 50px 40px 100px;
    overflow: visible;
    position: relative;
}
.progress .progress-title{
    display: block;
    font-size: 18px;
    font-weight: 700;
    color: #000000;
    position: absolute;
    bottom: -3px;
    left: -90px;
}
.progress .progress-bar{
    background: #fff;
    box-shadow: none;
    border-radius: 15px 0 0 15px;
    position: relative;
    -webkit-animation: animate-positive 2s;
    animation: animate-positive 2s;
}
.progress .progress-bar:before{
    content: "";
    border-top: 20px solid transparent;
    border-bottom: 20px solid transparent;
    position: absolute;
    top: -10px;
    right: -20px;
}
.progress .progress-value{
    display: block;
    font-size: 18px;
    font-weight: 700;
    color: #000000;
    position: absolute;
    bottom: -5px;
    right: -50px;
}
.progress .pink .progress-bar:before{ border-left: 20px solid var(--main-color); }
.progress .blue .progress-bar:before{ border-left: 20px solid var(--main-color); }
.progress .green .progress-bar:before{ border-left: 20px solid var(--main-color); }
.progress .orange .progress-bar:before{ border-left: 20px solid var(--main-color); }
.progress .red .progress-bar:before{ border-left: 20px solid var(--main-color); }
.progress .black .progress-bar:before{ border-left: 20px solid var(--main-color); }
@-webkit-keyframes animate-positive{
    0% { width: 0; }
}
@keyframes animate-positive{
    0% { width: 0; }
}
</style>