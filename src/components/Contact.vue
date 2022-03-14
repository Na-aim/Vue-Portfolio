<template>
 <h1 class="heading"> Contact <span> Me </span> </h1>
<div class="boxed">
 <div class="form-bg">
     
    <div class="container">
        <div class="row">
            <div class="col-md-12">
                <div class=" form-container">
                    <!-- <div class="form-icon">
                        <i class="fa fa-envelope-open"></i>
                    </div> -->
                    <form class="form-horizontal" @submit.prevent="handleSubmit">
                        <h3 class="title">Contact Me</h3>
                        <div class="form-group">
                            <span class="input-icon"><i class="fa fa-user"></i></span>
                            <input class="form-control" type="text" placeholder="Name" name="name" required v-model="name">
                        </div>
                        <div class="form-group">
                            <span class="input-icon"><i class="fa fa-envelope"></i></span>
                            <input class="form-control" type="email" placeholder="Email Address" name="Email" required v-model="email">
                        </div>
                        <div class="form-group">
                            <textarea class="form-control" rows="4" cols="120" placeholder="Message" name="message" required v-model="message"></textarea>
                        </div>
                        <button class="btn signin" type="submit">Send Message <i class="fa fa-long-arrow-alt-right"></i></button>
                    </form>
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
            email: '',
            name: '',
            message: '',
        }
    },
    methods: {
        handleSubmit() {
            console.log('this.name, this.email, this.message') 
            fetch(' https://express-backend1.herokuapp.com/contact', {
  method: 'POST',
  body: JSON.stringify({
    name: this.name,
    email: this.email,
    message: this.message,
  }),
  headers: {
    'Content-type': 'application/json; charset=UTF-8',
  },
})
  .then((response) => response.json())
  .then((json) => alert(json.msg))
  .catch((e) =>alert(e.msg));
        }
    }

}
</script>

<style>
.boxed{
    padding-top:40px ;
    padding-bottom: 50px;
    /* padding-left: 10rem;
    padding-right: 10rem; */
}

.form-container{
    font-family: 'Roboto', sans-serif;
    padding: 40px 40px 0 0;
    /* position: relative */
    display: grid;
    justify-content: center;
    
    
}
.form-container .form-icon{
    color: var(--main-color);;
    background-color: #fff;
    font-size: 40px;
    text-align: center;
    line-height: 80px;
    height: 80px;
    width: 80px;
    border: 3px solid var(--main-color);;
    border-radius: 50% 50% 50% 0;
    box-shadow: 0 0 20px rgba(0,0,0,0.3);
    position: absolute;
    top: 0;
    right: 0;
    z-index: 1;
}
.form-container .form-horizontal{
    background: linear-gradient(#e7e7e7 25px,rgba(255,255,255,0.97) 25px);
    padding: 40px 20px 20px;
    box-shadow: 0 0 20px -5px rgba(0,0,0,0.3);
    border-radius: 15px;
    
}
.form-container .title{
    color: #222;
    font-size: 27px;
    font-weight: 600;
    text-transform: capitalize;
    letter-spacing: 0.5px;
    margin: 0 0 20px;
}
.form-container .title:after{
    content: '';
    background-color: var(--main-color);;
    height: 3px;
    width: 110px;
    margin: 10px 0 0;
    display: block;
    clear: both;
}
.form-horizontal .form-group{
    background-color: rgba(255,255,255,0.15);
    margin: 0 0 15px;
    border-bottom: 2px solid #e7e7e7;
}
.form-horizontal .input-icon{
    color: var(--main-color);;
    font-size: 20px;
    text-align: center;
    line-height: 35px;
    height: 35px;
    width: 30px;
    margin: 0 0 0 4px;
    vertical-align: top;
    display: inline-block;
}
.form-horizontal .form-control{
    color: #222;
    background-color: transparent;
    font-size: 15px;
    font-weight: 400;
    letter-spacing: 1px;
    width: calc(100% - 40px);
    height: 33px;
    padding: 3px 10px 0 0;
    box-shadow: none;
    border: none;
    border-radius: 0;
    display: inline-block;
    transition: all 0.3s;
}
.form-horizontal textarea.form-control{
    height: auto;
    width: 100%;
}
.form-horizontal .form-control:focus{
    box-shadow: none;
    border: none;
}
.form-horizontal .form-control::placeholder{
    color: #b5b5b5;
    font-size: 15px;
    font-weight: 400;
    text-transform: capitalize;
}
.form-horizontal .btn{
    color: #d1d1d1;
    background-color: #fff;
    font-size: 15px;
    font-weight: 500;
    text-transform: uppercase;
    letter-spacing: 1px;
    padding: 10px 15px 7px 20px;
    margin: 0 auto;
    border: 2px solid #e7e7e7;
    border-radius: 20px;
    display: block;
    transition: all 0.3s ease 0s;
}
.form-horizontal .btn:hover,
.form-horizontal .btn:focus{
    color: var(--main-color);;
    background-color: #fff;
    border: 2px solid var(--main-color);;
}
.form-horizontal .btn i{ transition: all 0.3s ease 0s; }
.form-horizontal .btn:hover i{
    color: var(--main-color);;
    transform: translateX(3px);
}
</style>