---
layout: post
title: About
permalink: /about/
comments: true
---

## As a conversation Starter

All my life, I have lived here in San Diego, California, but the three flags I find that also represent me are: the Indonesian flag, Chinese flag, and American flag

<comment>
Flags are made using Wikipedia images
</comment>

<style>
    /* Style looks pretty compact, 
       - grid-container and grid-item are referenced the code 
    */
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); /* Dynamic columns */
        gap: 10px;
    }
    .grid-item {
        text-align: center;
    }
    .grid-item img {
        width: 100%;
        height: 100px; /* Fixed height for uniformity */
        object-fit: contain; /* Ensure the image fits within the fixed height */
    }
    .grid-item p {
        margin: 5px 0; /* Add some margin for spacing */
    }

    .image-gallery {
        display: flex;
        flex-wrap: nowrap;
        overflow-x: auto;
        gap: 10px;
        }

    .image-gallery img {
        max-height: 150px;
        object-fit: cover;
        border-radius: 5px;
    }
</style>

<!-- This grid_container class is used by CSS styling and the id is used by JavaScript connection -->
<div class="grid-container" id="grid_container">
    <!-- content will be added here by JavaScript -->
</div>

<script>
    // 1. Make a connection to the HTML container defined in the HTML div
    var container = document.getElementById("grid_container"); // This container connects to the HTML div

    // 2. Define a JavaScript object for our http source and our data rows for the Living in the World grid
    var http_source = "https://upload.wikimedia.org/wikipedia/commons/";
    var living_in_the_world = [
        {"flag": "0/01/Flag_of_California.svg", "greeting": "Hey", "description": "California - a very beautiful place and where I was born and raised :)"},
        {"flag": "9/9f/Flag_of_Indonesia.svg", "greeting": "Halo", "description": "Indonesia - where my parents came from"},
        {"flag": "f/fa/Flag_of_the_People%27s_Republic_of_China.svg", "greeting": "你好", "description": "China - where my grandparents came from"},  
        {"flag": "a/a4/Flag_of_the_United_States.svg", "greeting": "'Ey, how you doing?", "description": "America - the land and counrty where I was born and raised in"},  
    ];

    // 3a. Consider how to update style count for size of container
    // The grid-template-columns has been defined as dynamic with auto-fill and minmax

    // 3b. Build grid items inside of our container for each row of data
    for (const location of living_in_the_world) {
        // Create a "div" with "class grid-item" for each row
        var gridItem = document.createElement("div");
        gridItem.className = "grid-item";  // This class name connects the gridItem to the CSS style elements
        // Add "img" HTML tag for the flag
        var img = document.createElement("img");
        img.src = http_source + location.flag; // concatenate the source and flag
        img.alt = location.flag + " Flag"; // add alt text for accessibility

        // Add "p" HTML tag for the description
        var description = document.createElement("p");
        description.textContent = location.description; // extract the description

        // Add "p" HTML tag for the greeting
        var greeting = document.createElement("p");
        greeting.textContent = location.greeting;  // extract the greeting

        // Append img and p HTML tags to the grid item DIV
        gridItem.appendChild(img);
        gridItem.appendChild(description);
        gridItem.appendChild(greeting);

        // Append the grid item DIV to the container DIV
        container.appendChild(gridItem);
    }
</script>

### Journey through Life

Here is what I have done throughout my life so far:
- 🏫📚The preschool I went to was kidscare club
- 🏫📚From Kindergarden to eighth grade I have been to the same school, Design39 2016-2025
- 🏫📚I attend Del Norte High School and am in the ninth grade 2025-2026
- 

### Culture, Family, and Fun

Everything for me, revolves around family and my passions.

- I am of three ethnicities being born in America as a Chinese-Indonesian
- My parents were both born in Chinese-Indonesians born in Indonesia, and immigrated to America for college
- My parents both went to the University of Washington for college

<comment>
Gallery of Pics, scroll to the right for more ...
</comment>
<div class="image-gallery">
  <img src="{{site.baseurl}}/images/about/Lingloongfamily.jpg" alt="Image 1">
  <img src="{{site.baseurl}}/images/about/Boba.jpg" alt="Image 2">  
  <img src="{{site.baseurl}}/images/about/GrumpyBoba.jpg" alt="Image 3">
  <img src="{{site.baseurl}}/images/about/MeandPapa.jpg" alt="Image 4">
  <img src="{{site.baseurl}}/images/about/Plane.jpg" alt="Image 5">
</div>

### Return to Index

<div style="display: flex; flex-wrap: wrap; gap: 10px; margin: 15px 0;">
    <a href="{{site.baseurl}}/index" style="text-decoration: none;">
        <div style="background-color: #2413c0ff; color: yellow; padding: 10px 20px; border-radius: 5px; font-weight: bold;">
            Index
        </div>
    </a>
</div>