<template>
<div class="boxddd">
 <div class="home" id="home">
<div class="content">
<span class="hi"> hi there... </span>
<h3> i am <span> na-aim fredericks </span> </h3>
<p class="info"> i am a web developer </p>
<p class="text"> </p>

</div>
<div class="image">
<img src="../assets/pic.jpg" alt=" A pictuer of me ">
</div>
</div>

</div>
   
  
</template>

<script>
export default {

}
</script>

<style>
.boxddd{
    padding-left: 10rem;
    padding-right: 10rem;
}

.home{
    padding: 1rem 5%;
    min-height: 100vh;
    
}

.home{
display: flex;
align-items: center;
flex-wrap: wrap;
gap: 1.5rem;
}

.home .image{
flex:1 1 40rem;
object-fit: cover;
}
.home .image img{
width:100%;
} 
.home .content{
flex:1 1 40rem;
}

.home .content .hi{
font-size: 2rem;
color:var(--main-color);
}
.home .content h3{
font-size: 4.5rem;
color:#111;
text-transform: uppercase;
}

.home .content h3 span{
color:var(--main-color);
text-transform: uppercase;
}

.home .content .info{
font-size: 2.5rem;
color:#111;
padding:.5rem 0;
}
.home .content .text{
font-size: 1.7rem;
color: #666;
padding:.5rem 0;
}


</style>