<template>
 <h1 class="heading"> My <span> Resume </span> </h1>
  <div class="containe">
     
    <div class="row">
        <div class="main-timeline">
            <div class="timeline">
                <div class="timeline-icon"></div>
                <div class="timeline-content">
                    <span class="date"> 2014 - 2019</span>
                    <h5 class="title">Nationaltion Senior Certificate</h5>
                    <p class="description">
                         Got my national senior certificate at Oval North High Secondery.
                    </p>
                </div>
            </div>
 
            <div class="timeline">
                <div class="timeline-icon"></div>
                <div class="timeline-content">
                    <span class="date">Feb 2020 - Feb 2021</span>
                    <h5 class="title">Volunteering at an ECD</h5>
                    <p class="description">
                        Provided children with opportunities to develop fundamental movement skills by leading activities that focus on physical literacy and expanding their minds with numeracy.
                    </p>
                </div>
            </div>
             <div class="timeline">
                <div class="timeline-icon"></div>
                <div class="timeline-content">
                    <span class="date">May 2021 - Sep 2021</span>
                    <h5 class="title">Retail and wholesale student NQF L3</h5>
                    <p class="description">
                        Did a learnership at Passionat about People "PAP" which consisted of 4 months theory on retail and wholesale and month of practical which was at Levi in Waterfront.
                    </p>
                </div>
            </div>
             <div class="timeline">
                <div class="timeline-icon"></div>
                <div class="timeline-content">
                    <span class="date">Sep 2021 -  2023</span>
                    <h5 class="title">Life Choices Academy</h5>
                    <p class="description">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum mattis felis vitae risus pulvinar tincidunt. Nam ac venenatis enim. Aenean hendrerit justo sed.
                    </p>
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
#39b3ff
<style>
.containe{
    /* display: flex;
    justify-content: center !important; */
    padding-top: 100px;
    padding-left: 10rem;
    padding-right: 10rem;
}
.main-timeline{
    overflow: hidden;
    position: relative;
    padding: 60px 0;
}
.main-timeline:before{
    content: "";
    width: 1px;
    height: 100%;
    background: #cfcdcd;
    position: absolute;
    top: 0;
    left: 50%;
}
.main-timeline .timeline{
    width: 50%;
    clear: both;
    position: relative;
}
.main-timeline .timeline:before,
.main-timeline .timeline:after{
    content: "";
    display: block;
    clear: both;
}
.main-timeline .timeline:first-child:before,
.main-timeline .timeline:last-child:before{
    content: "";
    width: 11px;
    height: 11px;
    background: #ff0000;
    box-sizing: content-box;
    border: 5px solid #fff;
    box-shadow: 0 0 0 2px #ff0000;
    position: absolute;
    top: -54px;
    right: -11px;
    transform: rotate(45deg);
}
.main-timeline .timeline:last-child:before{
    top: auto;
    bottom: -54px;
}
.main-timeline .timeline:last-child:nth-child(even):before{
    right: auto;
    left: -11px;
}
.main-timeline .timeline-icon{
    width: 24px;
    height: 24px;
    background: #fff;
    border: 1px solid #cfcdcd;
    position: absolute;
    top: 17px;
    right: -13px;
    z-index: 1;
    transform: rotate(45deg);
}
.main-timeline .timeline-icon:before{
    content: "";
    display: block;
    width: 15px;
    height: 15px;
    background: #fff;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    transition: background-color 0.2s ease 0s;
}
.main-timeline .timeline:hover .timeline-icon:before{ background: var(--main-color); }
.main-timeline .timeline-content{
    width: 85%;
    padding: 18px 30px;
    background: #fff;
    text-align: right;
    float: left;
    border: 1px solid transparent;
    position: relative;
    transition: all 0.3s ease 0s;
}
.main-timeline .timeline:hover .timeline-content{
    border: 1px solid #cfcdcd;
}
.main-timeline .timeline-content:before{
    content: "";
    display: block;
    width: 14px;
    height: 14px;
    background: #fff;
    border: 1px solid #cfcdcd;
    position: absolute;
    top: 21px;
    right: -7.3px;
    transform: rotate(45deg);
    transition: all 0.2s ease 0s;
}
.main-timeline .timeline:hover .timeline-content:before{
    background: var(--main-color);
    border-color: var(--main-color);
}
.main-timeline .timeline-content:after{
    content: "";
    width: 11%;
    height: 1px;
    background: #cfcdcd;
    position: absolute;
    top: 28px;
    right: -14%;
}
.main-timeline .date{
    display: block;
    font-size: 15px;
    font-weight: 600;
    color: var(--main-color);
    margin: 0 0 8px;
    transition: all 0.3s ease 0s;
}
.main-timeline .timeline:hover .date{ color: #444; }
.main-timeline .title{
    font-size: 18px;
    color: #444;
    margin-top: 0;
    transition: all 0.3s ease 0s;
}
.main-timeline .timeline:hover .title{ color: var(--main-color); }
.main-timeline .description{
    font-size: 16px;
    color: rgb(0, 0, 0);
    line-height: 28px;
    margin-top: 8px;
}
.main-timeline .timeline:nth-child(2n),
.main-timeline .timeline:nth-child(2n) .timeline-content{
    float: right;
    text-align: left;
}
.main-timeline .timeline:nth-child(2n) .timeline-icon{
    right: 0;
    left: -12px;
}
.main-timeline .timeline:nth-child(2n) .timeline-content:before{ left: -7.3px; }
.main-timeline .timeline:nth-child(2n) .timeline-content:after{ left: -14%; }
@media only screen and (max-width: 767px){
    .main-timeline{ padding-left: 20px; }
    .main-timeline:before{ left: 20px; }
    .main-timeline .timeline{ width: 100%; }
    .main-timeline .timeline,
    .main-timeline .timeline-content{
        float: right;
        text-align: left;
    }
    .main-timeline .timeline:first-child:before,
    .main-timeline .timeline:last-child:nth-child(odd):before{
        right: auto;
        left: -11px;
    }
    .main-timeline .timeline-icon{
        right: 0;
        left: -12px;
    }
    .main-timeline .timeline-content:before{ left: -7.3px; }
    .main-timeline .timeline-content:after{ left: -14%; }
}
</style>