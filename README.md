# Website_CSS
The complimentary part of the website that is responsible for colors animation and general adjustments.
/* Auther: Sherif Hamed */
/* Start Variables */
:root {
  --main-color: #10cab7;
  --secondary-color: #2c4755;
  --section-padding: 60px;
  --section-background: #f6f6f6;
  --main-duration: 0.5s;
}
/* End Variables */
/* Chosen Google font */
body {
  font-family: "Work Sans", sans-serif;
}
.container {
  padding-left: 15px;
  padding-right: 15px;
  margin-left: auto;
  margin-right: auto;
}
/* Based on the screen type used */

/* Small */
@media (min-width: 768px) {
  .container {
    width: 750px;
  }
}
/* Medium */
@media (min-width: 992px) {
  .container {
    width: 970px;
  }
}
/* Large */
@media (min-width: 1200px) {
  .container {
    width: 1170px;
  }
}
.header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 999;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background: rgb(255, 255, 255);
  box-shadow: var(--box-shadow);
  border: 4px dashed gainsboro;
}
.item {
  font-size: larger;
  font-family: fantasy;
  color: #0d0d0e;
  display: flex;
  justify-content: space-between;
  align-items: center;
  /* flex-wrap: wrap; */
  position: relative;
  list-style: none;
  text-decoration: none;
  text-decoration-style: none;
}

.header .item i {
  cursor: pointer;
}
.header a:hover {
  display: block;
  background-color: rgb(133, 185, 168);
  text-decoration-style: none;
  text-decoration: none;
  border-style: 2px;
  transition: 0.3s;
}

.logo {
  color: var(--main-color);
  font-size: 26px;
  font-weight: bold;
  height: 72px;
  display: flex;
  /* justify-content: center;
  align-items: center; */
}

.button {
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
  font-size: large;
  align-items: center;
  margin-top: 25px;
  margin-left: 110px;
  border-radius: 20px;

  cursor: pointer;
}
.button:hover {
  background-color: #3ca0be;
}
/* Start Landing temp2 */
.landing-landing {
  position: relative;
}
.landing-landing::before {
  content: "";
  position: absolute;
  left: 0;
  top: -40px;
  width: 100%;
  height: 100%;
  background-color: #63e9d7;
  z-index: -1;
  transform: rotate(20deg);
  transform-origin: top left;
}
.landing-landing .container {
  min-height: calc(100vh - 72px);
  display: flex;
  align-items: center;
  padding-bottom: 120px;
}
.landing-landing .text {
  flex: 1;
}
@media (max-width: 991px) {
  .landing-landing .text {
    text-align: center;
  }
}
.landing-landing .text h1 {
  font-size: 40px;
  margin: 0;

  /* letter-spacing: -2px; */
}
@media (max-width: 767px) {
  .landing .text h1 {
    font-size: 28px;
  }
}
.landing-landing .text p {
  font-size: 23px;
  line-height: 1.7;
  margin: 5px 0 0;
  color: #666;
  max-width: 500px;
  text-align: center;
}
@media (max-width: 991px) {
  .landing-landing .text p {
    margin: 10px auto;
  }
}
@media (max-width: 767px) {
  .landing-landing .text p {
    font-size: 18px;
  }
}
.landing-landing .image img {
  position: relative;
  width: 600px;
  animation: up-and-down 5s linear infinite;
  border-radius: 30px;
  z-index: -1;
}
@media (max-width: 991px) {
  .landing-landing .image {
    display: none;
  }
}
.landing-landing .go-down {
  color: brown;
  position: absolute;
  bottom: 90px;
  left: 50%;
  transform: translateX(-50%);
  transition: var(--main-transition);
}
.landing-landing .go-down:hover {
  color: #63e9d7;
}

.landing-landing .go-down i {
  animation: bouncing 1.5s infinite;
}
/* Animation start */
@keyframes up-and-down {
  0%,
  100% {
    top: 0;
  }
  50% {
    top: -50px;
  }
}
@keyframes bouncing {
  0%,
  10%,
  20%,
  50%,
  80%,
  100% {
    transform: translateY(-2.1rem);
  }
  40%,
  60% {
    transform: translateY(-15px);
  }
}
/* Stand Alone image start */
.landing {
  background-image: url(solidWaste.png);
  background-size: cover;
  height: calc(100vh);
}

/* End Main Photo */

/* Feature Start */
.features {
  padding-top: 60px;
  padding-bottom: 60px;
  position: relative;
  background-color: white;
}
.features .container {
  min-height: calc(100vh - 80px);
  /* display: flex; */
  /* align-items: center; */
  padding-bottom: 120px;
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 40px;
}
.features .box {
  text-align: center;
  border: 1px dashed rgb(212, 9, 9);
}
.features .box .img-holder {
  position: relative;
  overflow: hidden;
}
.features .box .img-holder::before {
  content: "";
  position: absolute;
  left: 0;
  top: -1px;
  width: 100%;
  height: 100%;
}
.features .box .img-holder::after {
  content: "";
  position: absolute;
  bottom: 0;
  right: 0;
  border-style: solid;
  border-width: 0px 0px 150px 500px;
  border-color: transparent transparent white transparent;
  transition: var(--main-transition);
}
.features .box .img-holder img {
  max-width: 100%;
}

.features .box:hover .img-holder::after {
  border-width: 170px 500px 170px 0;
}
.features .box h2 {
  position: relative;
  font-size: 40px;
  margin: auto;
  width: fit-content;
}
.features .box h2::after {
  content: "";
  position: absolute;
  bottom: -20px;
  left: 15px;
  height: 5px;
  width: calc(100% - 30px);
}
.features .box p {
  line-height: 2;
  font-size: 20px;
  margin: 30px 0;
  padding: 25px;
  color: #777;
}
.features .box a {
  display: block;
  border: 3px solid transparent;
  width: fit-content;
  margin: 0 auto 30px;
  font-weight: bold;
  font-size: 22px;
  padding: 10px 30px;
  border-radius: 6px;
  transition: var(--main-transition);
}
.features .quality .img-holder::before {
  background-color: rgb(244 64 54 / 60%);
}
.features .quality h2::after {
  background-color: #f44036;
}
.features .quality a {
  color: #f44036;
  border-color: #f44036;
  background: linear-gradient(to right, #f44036 50%, white 50%);
  background-size: 200% 100%;
  background-position: right bottom;
  padding-top: -50px;
}
.features .time .img-holder::before {
  background-color: rgb(0 150 136 / 60%);
}
.features .time h2::after {
  background-color: #009688;
}
.features .time a {
  color: #009688;
  border-color: #009688;
  background: linear-gradient(to right, #009688 50%, white 50%);
  background-size: 200% 100%;
  background-position: right bottom;
}
.features .passion .img-holder::before {
  background-color: rgb(3 169 244 / 60%);
}
.features .passion h2::after {
  background-color: #03a9f4;
}
.features .passion a {
  color: #03a9f4;
  border-color: #03a9f4;
  background: linear-gradient(to right, #03a9f4 50%, white 50%);
  background-size: 200% 100%;
  background-position: right bottom;
}
.features .box:hover a {
  background-position: left bottom;
  color: white;
}
#quality:hover {
  transform: translateY(-70px);
  box-shadow: 0 2px 15px rgb(0 0 0 / 20%);
}
#time:hover {
  transform: translateY(-70px);
  box-shadow: 0 2px 15px rgb(0 0 0 / 20%);
}
#passion:hover {
  transform: translateY(-70px);
  box-shadow: 0 2px 15px rgb(0 0 0 / 20%);
}
/* Feature end */

/* END Features */
/* ---------------------------- */
/* Start spatial haeding */
.special-heading {
  font-size: 100px;
  font-weight: 800;
  text-align: center;
  color: burlywood;
  margin: 0;
}
/*to Choose the next paragraph only */
.special-heading + p {
  margin: -10px 0 0;
  text-align: center;
  font-size: 20px;
}
/* End spatial heading */

/* Start Services */
.services {
  padding-top: var(--section-padding);
  padding-bottom: var(--section-padding);
}
.services .services-content {
  /* background-image: url(./waste.jpg); */
  /* background-image: linear-gradient(rgb(0, 0, 0, 0.3)); */
  /* background-size: cover; */
  /* background-repeat: no-repeat; */
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  grid-gap: 40px;
  margin-top: 100px;
}
/* #effective {
  margin-left: 330px;
  text-align: left;
  flex: 1;
  padding-left: 90px;
  size-adjust: 100px;
} */
.services .services-content .srv {
  display: flex;
  margin-bottom: 40px;
}
@media (max-width: 767px) {
  .services .services-content .srv {
    flex-direction: column;
    text-align: center;
  }
}
.services .services-content .srv i {
  color: var(--main-color);
  flex-basis: 60px;
}
.services .services-content .srv .text {
  flex: 1;
}
.services .services-content .srv .text h3 {
  margin: 0 0 20px;
}
.services .services-content .srv .text p {
  color: #444;
  font-weight: 300;
  line-height: 1.6;
}
.services .services-content .image {
  text-align: center;
  position: relative;
}
.services .services-content .image::before {
  content: "";
  background-color: var(--secondary-color);
  width: 100px;
  height: calc(100% + 100px);
  top: -50px;
  position: absolute;
  right: 0;
  z-index: -1;
}
.services .services-content .image img {
  width: 260px;
}
@media (max-width: 1199px) {
  .image-column {
    display: none;
  }
}
/* End Services */
/* Footer start */
.footer {
  padding-top: 25px;
  padding-bottom: 25px;
  background: rgb(175, 164, 164);
}
.footer .box-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  grid-gap: 30px;
}
.footer .box-container .box h3 {
  font-size: 24px;
  color: var(--black);
  margin: 20px;
  padding: 30px;
}
.footer .box-container .box h3 i {
  color: black;
}
.footer .box-container .box .links {
  display: block;
  font-size: 16px;
  color: #000000;
  padding: 12px;
}
.box .Naming {
  width: 400px;
}
#Naming {
  font-weight: 900;
  font-size: 550;
  padding: 40px;
}
#Naming + p {
  font-weight: 400;
  font-size: 550;
  padding: 20px;
}
.footer .box-container .box .links {
  display: block;
  font-size: 16px;
  color: var(--light-color);
  padding: 10px;
  text-align: center;
}
.footer .box-container .box h3 {
  color: brown;
  text-align: center;
}
.footer .box-container .box .share a {
  margin-left: 20px;
  height: 70px;
  width: 70px;
  line-height: 4rem;
  border-radius: 20px;
  font-size: 30px;
  color: var(--black);
  margin-right: 0.2rem;
  background: #eee;
  text-align: center;
}

/* Footer ends */
/* video section start */
.video {
  position: relative;
}
.video::before {
  content: "";
  position: absolute;
  left: 0;
  top: -40px;
  width: 100%;
  height: 100%;
  background-color: #07070734;
  z-index: -1;
  transform: rotate(-12deg);
  transform-origin: bottom right;
}
.video .container {
  min-height: calc(100vh - 72px);
  /* display: flex; */
  align-items: center;
  padding-bottom: 120px;
  padding-right: 60px;
  background-color: rgb(133, 236, 223);
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
}
.video .text {
  align-items: center;
  flex: 1;
  /* margin-left: -30px; */
  text-align: center;
  border-radius: 52px;
  border: 1px solid rgb(212, 9, 9);
  padding-left: 30px;
}
@media (max-width: 991px) {
  .video .text {
    text-align: center;
  }
}
.video .text h1 {
  font-size: 60px;
  /* margin-right: 10; */
  /* padding-left: -10px; */
  text-align: center;

  /* letter-spacing: -2px; */
}
/* @media (max-width: 767px) {
  .landing .text h1 {
    font-size: 28px;
  }
} */
.video .text p {
  font-size: 23px;
  line-height: 1.7;
  margin: 5px 0 0;
  color: #666;
  max-width: 500px;
  text-align: center;
  padding-top: -50px;
}
@media (max-width: 991px) {
  .video .text p {
    margin: 10px auto;
  }
}
@media (max-width: 767px) {
  .video .text p {
    font-size: 18px;
  }
}
/* .video .image img {
  position: relative;
  width: 600px;
  animation: up-and-down 5s linear infinite;
  border-radius: 30px;
  z-index: -1;
} */
@media (max-width: 991px) {
  .video .myvideo {
    display: none;
  }
}
.myvideo video {
  display: flex;
  height: 700px;
  width: 600px;
}
.video .text:hover {
  background: #10cab7;
  transform: translateX(-50px);
  /* transform: rotate(0.5turn); */
  box-shadow: 0 2px 15px rgb(0 0 0 / 20%);
  border-start-end-radius: 50px;
}
/* video section end */
