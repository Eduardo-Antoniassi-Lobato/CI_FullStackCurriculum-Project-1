![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)

Project 1 - Full Stack Curriculum - Code Institute

Student: Eduardo Antuniassi Lobato

M. Arahant is an imaginary Project to connect modern people to ancient knowledge, now with a focus on buddhism. Most times teachings or knowledge connected to a religion, as here in this case, is wrogly judged and misunderstood. The core of what is today called buddhism is based mostly on logical and psychalogical observations on matters that permeates our everyday reality. Concepts like the nature of mind, how to concentrate in an effective way and exercices to develop all these concepts through own experience are present in these teachings.

The idea of the project is to bring this content through texts, maybe in the future videos and self-developed apps.

The web site is separated in three parts:

Index-Page: With description of the idea of the project.

wisdom-drops-Page: where some of this knowledge can be read.

Contact-Page: with a sign up form to a newsletter, location of an imaginary space and a link to google store to the apps developed by the project.

Code used form external sources:

My header and footer where mainly based on the Love running Project present in this course:

Original Header Code:

<header>
        <a href="index.html">
        <h1 id="logo">Love Running</h1>   
    </a>
    <nav>
        <ul id="menu">
            <li>
                <a href="signup.html">Sign Up</a>
            </li>
            <li>
                <a href="gallery.html">Gallery</a>
            </li>           
            <li> 
                <a href="index.html" class="active">Home</a>
            </li>
        </ul>
    </nav>
    </header>

 Original styles:

h1, h2 {
    font-family: Oswald, sans-serif;
    text-transform: uppercase;
    letter-spacing: 4px;
    color: #252525;
}
   
#logo {
    float: left;
    font-size: 280%;
    margin-left: 30px;
}

/* navigation links */
#menu {
    font-size: 110%;
    letter-spacing: 4px;
}

#menu, #logo {
    line-height: 75px;
}

#menu li {
    float: right;
    list-style-type: none;
    margin-right: 30px;
}

#menu a {
    text-decoration: none;
    color: inherit;
}

#menu a:hover {
    border-bottom: 1px solid #3a3a3a;
}

.active {
    border-bottom: 1px solid #3a3a3a;
}

Print screen of modified version in this project:

![Header-image](./assets/images/Header-print.png)

![Footer-image](./assets/images/Footer-print.png)

The animation section were based on Annie Huang's git hub repository.

Original Code:

h1 {
  font-size: clamp(1rem, 3vw + 1rem, 4rem);
  position: relative;
  font-family: "Source Code Pro", monospace;
  position: relative;

/*  // If you don't have the display: grid, place-content and text-align version in the body,
  // you can still control the h1 width (default is full width 100%) by using the max-content value.
  outline: 2px solid red;
  width: max-content;*/

}

h1::before,
h1::after {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
}

h1::before {
  background: var(--bg-color);

  /* the forwards keyword means it doesn't go back to the start position */
  /*animation: typewriter 1s ease forwards; */

  /* steps will make it jump every characters (we got total 24 characters), Very nice effect, didn't know we can do that.*/
  /* Give a 1s delay make the type writer (blink effect) more mirroring to a 'ready to type' effect. */
  animation: typewriter var(--typewriterSpeed) steps(var(--typewriterCharacters)) 1s forwards;
}

h1::after {
  width: 0.125em;
  background: black;
  animation:
    typewriter var(--typewriterSpeed) steps(var(--typewriterCharacters)) 1s forwards,
    blink 750ms steps(var(--typewriterCharacters)) infinite; /* I found it can go without step(24), but with the step(24) here it the jumping on the blink effect is more prominent */
}

.subtitle {
  color: hsla(0, 0%, 0%, 0.7);
  font-size: 2rem;
  font-weight: 400;
  opacity: 0;
  transform: translateY(3rem);
  animation: fadeInUp 2s ease calc(var(--typewriterSpeed) + 2s) forwards;
}


@keyframes typewriter {
  /* If your start position is the same as your initial value of the page layout, then you don't need to have a from in the keyframe */
  to {
    left: 100%;
  }
}

@keyframes blink {
  to {
    background: transparent;
  }
}

@keyframes fadeInUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

Final result on this project:

![Animation](./assets/images/Animation-print.png)


The form section of this web site were also based on the respective one of Love Running course Module.

Original Code:

<section class="form-section">
        <form method="POST" action="https://formdump.codeinstitute.net/" class="signup-form">
            <h2>Let's get you signed up! <i class="fas fa-heartbeat"></i></h2>
            <label for="fname">First Name</label>
            <input class="text-input" id="fname" name="first_name" type="text" required>
            
            <label for="lname">Last Name</label>
            <input class="text-input" id="lname" name="last_name" type="text" required>
            
            <label for="email">Email Address</label>
            <input class="text-input" type="email" id="email" name="email_address" required>
            
            <label for="road" class="b" >Road</label>
            <input type="radio" class="radio-button" id="road" name="running_preference" value="road" required>
            <label for="trail">Trail</label>
            <input type="radio" class="radio-button" id="trail" name="running_preference" value="trail" required>
            <label for="both">Both</label>
            <input type="radio" class="radio-button" id="both" name="running_preference" value="both" required>
            
            <input class="join-button"  type="submit" value="Let's Run!">
        </form>
    </section>

/*Form*/

.form-section {
    clear: left;
    background: url("https://codeinstitute.s3.amazonaws.com/FundamentalsProjects/HTML-CSS/formbg.webp");
    background-size: cover;
    background-position: center;
    height: 900px;
}

.signup-form {
    margin: 150px 10% 0 0;
    color: #fff;
    background-color: rgba(60, 60, 60, 0.6);
    max-width: 400px;
    position: absolute;
    left: 10%;
    padding: 30px;
}

.signup-form > h2 {
    color: #fafafa;
    margin-bottom: 20px;
}

.text-input {
    background: transparent;
    color: #fafafa;
    width: 100%;
    height: 25px;
    margin: 5px 0 20px 0;
    border: 1px solid #fafafa;
    border-radius: 2px; 
}

.text-input:hover {
    border-color: #f16c6b;
}

.radio-button {
    margin-right: 4px;
}

.join-button {
    margin-top: 20px;
    border-radius: 2px;
    padding: 15px 32px 15px 32px;
    text-align: center;
    font-size: 100%;
    background-color: #f16c6b;
    color: #fafafa;
    display: block;    
}

.join-button:hover {
    background-color: #fafafa;
    color: #f16c6b;
}


![Form](/assets/images/Form-print.png)


Web site address:

https://eduardo-antoniassi-lobato.github.io/CI_FullStackCurriculum-Project-1/
