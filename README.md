<strong>Hello everyone,</strong><br>

Front End Developer with 5+ yrs experience | Php | Javascript | MySQL | CSS3 | HTML5
https://www.linkedin.com/in/alessandro-tezza-5201a721a/<br>
https://www.alessandrotezza.it
@import url('https://fonts.googleapis.com/css?family=Concert+One&display=swap');

html, body {
  width: 100%;
  height: 100%;
  margin: 0;
}

html {
  font-size: 62.5%;
}

body {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: 'Concert One', cursive;
  font-size: 4.2rem;
  -webkit-font-smoothing: antialiased;
  text-rendering: optimizeLegibility;
}

svg {
  display: none;
}

.tabber {
  position: relative;
  display: flex;
  align-items: stretch;
  justify-content: stretch;
  
  label {
    user-select: none;
    padding: 3rem;
    cursor: pointer;
    will-change: transform;
    transform: translateZ(0px);
    transition:
      transform 125ms ease-in-out,
      filter 125ms ease-in-out;
    // filter: blur(.25rem);
    
    &:hover {
      transform: scale(1.15);
      // filter: blur(0px);
    }
  }
  
  input[type="radio"] {
    display: none;
    
    // static
    &#t1 ~ .blob {
      transform-origin: right center;
    }
    
    &#t2 ~ .blob {
      transform-origin: left center;
    }
    
    // animated
    &#t1:checked {
      
      ~ .blob {
        background: cornflowerblue;
        animation-name: stretchyRev;
      }
    }
    
    &#t2:checked {
      
      ~ .blob {
        background-color: skyblue;
        animation-name: stretchy;
      }
    }
  }
  
  .blob {
    top: 0;
    left: 0;
    width: 50%;
    height: 100%;
    position: absolute;
    z-index: -1;
    border-radius: 4rem;
    animation-duration: .5s;
    animation-direction: forwards;
    animation-iteration-count: 1;
    animation-fill-mode: forwards;
    transition:
      transform 150ms ease,
      background 150ms ease;
    filter: url("data:image/svg+xml;utf8,<svg xmlns=\"http://www.w3.org/2000/svg\" version=\"1.1\"><defs><filter id=\"goo\"><feGaussianBlur in=\"SourceGraphic\" stdDeviation=\"10\" result=\"blur\" /><feColorMatrix in=\"blur\" mode=\"matrix\" values=\"1 0 0 0 0  0 1 0 0 0  0 0 1 0 0  0 0 0 19 -9\" result=\"goo\" /><feComposite in=\"SourceGraphic\" in2=\"goo\" operator=\"atop\"/></filter></defs></svg>#goo");
    
    &:before, &:after {
      display: block;
      content: "";
      position: absolute;
      top: 0;
      background-color: inherit;
      height: 100%;
      width: 50%;
      border-radius: 100%;
      transform: scale(1.15);
      transition: transform 150ms ease;
      animation-name: pulse;
      animation-duration: .5s;
      animation-iteration-count: infinite;
      animation-direction: alternate;
    }
    
    &:before {
      left: 0;
      animation-delay: .15s;
    }
    
    &:after {
      right: 0;
    }
  }
}

@keyframes stretchy {
  0% {
    transform: translateX(0) scaleX(1);
  }
  50% {
    transform: translateX(0) scaleX(2);
  }
  100% {
    transform: translateX(100%) scaleX(1);
  }
}

@keyframes stretchyRev {
  0% {
    transform: translateX(100%) scaleX(1);
  }
  50% {
    transform: translateX(0) scaleX(2);
  }
  100% {
    transform: translateX(0) scaleX(1);
  }
}

@keyframes pulse {
  0%, 50% {
    transform: scaleX(1);
  }
  25%, 75% {
    transform: scaleX(1.5);
  }
}
<form class="tabber">
  <label for="t1">Pizza</label>
  <input id="t1" name="food" type="radio" checked>
  <label for="t2">Tacos</label>
  <input id="t2" name="food" type="radio">
  <div class="blob"></div>
</form>

<!---
aletex1994/aletex1994 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
