---
title: "Moon"
date: 2025-11-10 20:53:01
lastmod: 2025-11-10 21:27:36
tags:
- Moon
- Javascript
---

## Moon?

I want to show the current moon phase here.
This'll be...interesting to do in Hugo.

{{< rawhtml >}}
<div class="moon_container">
    <div id="moon">
        testing
    </div>
    <script>
        document.addEventListener("DOMContentLoaded", function() {
            console.log("its WORKING");
            moon = document.getElementById("moon");
            if(moon) moon.textContent = "imthemoon";
        });
    </script>
</div>
{{< /rawhtml >}}
