---
layout: archive
title: "Learning Journal"
permalink: /journal/
author_profile: true
redirect_from:
  - /journal
# IMPORTANT: Remove or set custom_js to false to avoid double initialization
custom_js: false
---

<style>
/* Hide the vertical connector lines on timeline items */
.vis-item:after {
  display: none !important;
}
</style>

# My Learning Journey

<!-- Timeline Container -->
<div id="timeline" style="width: 100%; height: 500px;"></div>

<!-- Load Vis.js Library -->
<script src="https://unpkg.com/vis-timeline@7.4.6/standalone/umd/vis-timeline-graph2d.min.js"></script>
<link rel="stylesheet" href="https://unpkg.com/vis-timeline@7.4.6/styles/vis-timeline-graph2d.min.css">

{% raw %}
<!-- Timeline Script -->
<script>
document.addEventListener("DOMContentLoaded", function() {
    console.log("✅ DOMContentLoaded event fired. Initializing timeline...");

    // Get timeline container
    var container = document.getElementById("timeline");
    if (!container) {
        console.error("❌ Timeline container not found!");
        return;
    }
    console.log("✅ Timeline container found:", container);

    // Define groups for the timeline
    var groups = new vis.DataSet([
        { id: 1, content: "Courses", value: 1 },
        { id: 2, content: "Research", value: 2 },
        { id: 3, content: "Achievements", value: 3 }
    ]);

    // Define timeline events (items)
    var items = new vis.DataSet([
        { id: 1, group: 1, content: "Bayesian Networks Course", start: "2024-01" },
        { id: 2, group: 1, content: "ML & GIS Course", start: "2024-07" },
        { id: 3, group: 2, content: "Started Flood Research", start: "2024-06" },
        { id: 4, group: 2, content: "Reservoir Optimization Study", start: "2025-03" },
        { id: 5, group: 3, content: "Won Data Challenge", start: "2025-01" },
        { id: 6, group: 3, content: "Presented at GIS Day", start: "2024-11-20" }
    ]);




    // Timeline configuration options
    var options = {
        groupOrder: (a, b) => a.value - b.value,
        groupHeightMode: "fixed", // Force fixed group height
        groupMinHeight: 80,       // Set fixed height (in pixels)
        stack: true,
        showCurrentTime: true,
        zoomable: false,
        horizontalScroll: true,
        moveable: true,
        wheel: {
          zoomSpeed: 0,
          deltaSpeed: 1
        },
        height: "500px",
        margin: { item: 10 },
        start: "2023-01-01",
        end: "2026-12-31"
    };

        try {
        // Initialize timeline
//        var timeline = new vis.Timeline(container, items, options);
//        timeline.setGroups(groups);
//        console.log("✅ Timeline initialized successfully!");
//    } catch (error) {
//        console.error("❌ Timeline creation error:", error);
//        container.innerHTML = "Error loading timeline.";
//    }


});
</script>
{% endraw %}