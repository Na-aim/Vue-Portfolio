<template>
<div class="fit">
<div class="about" id="about">

<h1 class="heading"> about <span> me </span> </h1>

<div class="row-1">
<div class="image">
<img src="../assets/pic.jpg" alt="">
</div>
<div class="content">
<h3> My name is Na-aim Fredericks and i am a front-end developer </h3>
<p>I am Na-aim Fredericks and I love web development like who does not love the ability to create, and I demonstrate a strong power of analytical reasoning. The reason why i love web development is because front-end web development is an exciting career because it's always evolving and constantly changing.</p>
<div class="box-container">
    <div class="box">
        <p> <span> Age : </span> 22 </p>
        <p> <span> Gender : </span> male </p>
        <p> <span> Language : </span> english </p>
        <p> <span> Work : </span> front-end developer </p>
    </div>
    <div class="box">
        <p> <span>Freelance : </span> available </p>
        <p> <span> Phone : </span> 068-573-1144 </p>
        <p> <span> Email : </span> fredericksnaaim13@gmail.com </p>
        <p> <span> Country : </span> South Africa </p>
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

<style>
.fit{
    padding-top:100px ;
    padding-left: 10rem;
    padding-right: 10rem ;
}
.heading{
    font-size: 4rem;
    padding-bottom: 1rem;
    color: #111;
    text-transform: uppercase;
}
.heading span{
    color: var(--main-color);
    text-transform: uppercase;
}

.about .row-1{
display: flex;
flex-wrap: wrap;
gap:1.5rem;
padding-bottom: 2rem;
}
.about .row-1 .image{
flex:1 1 25rem;
}
.about .row-1 .image img{
height: 100%;
width:100%;
object-fit: cover;
border:1rem solid #fff;
border-radius: .5rem;
box-shadow: 0 .5rem 1rem rgba(0,0,0,.1);
}
.about .row-1 .content{
flex:1 1 50rem;
}

.about .row-1 .content h3{
color:#333;
font-size: 3.5rem;
}
.about .row-1 .content p{
color:#666;
font-size: 1.7rem;
padding:.5rem 0;
}
.about .row-1 .content .box-container{
display: flex;
flex-wrap: wrap;
gap:1.5rem;
padding: 5rem 0;
}
.about .row-1 .content .box-container .box{
flex:1 1 20rem;
}
.about .row-1 .content .box-container .box span{
color:var(--main-color); 
}

/* skills section */

</style>