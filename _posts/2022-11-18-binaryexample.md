---
title: Binary Example
layout: default
description: Example of Binary in Conditionals
permalink: /binary-example
image: /images/binary.png
categories: []
tags: [html, liquid, javascript]
---
<button id="firstButton" onclick="firstToggle()">0</button>
<button id="secondButton" onclick="secondToggle()">0</button>
<p id="conditionalOutput">True/False</p>
<script>
S      function firstToggle() {
        if (document.getElementById("firstButton").innerHTML = "0") {
          document.getElementById("firstButton").innerHTML= "1";
        }
        else if (document.getElementById("firstButton").innerHTML = "1") {
          document.getElementById("firstButton").innerHTML= "0";
        }
      }
      function secondToggle() {
        if (document.getElementById("secondButton").innerHTML = "0") {
          document.getElementById("secondButton").innerHTML= "1";
        }
        else if (document.getElementById("secondButton").innerHTML = "1") {
          document.getElementById("secondButton").innerHTML= "0";
        }
      }
      if (document.getElementById("firstButton").innerHTML = document.getElementById("secondButton")) {
        document.getElementById("conditionalOutput").innerHTML = "True"
      } else {
        document.getElementById("conditionalOutput").innerHTML = "False"f
      }
    </script>