---
layout: archive
title: "Learning Journal"
permalink: /journal/
author_profile: true
redirect_from:
- /journal
---
<style>
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
        { id: 1, content: "GIS/RS", value: 1 },
        { id: 2, content: "Coding", value: 2 },
        { id: 3, content: "Courses", value: 3 },
        { id: 4, content: "Studies", value: 4 }
    ]);

    // Define timeline events (items)
    var items = new vis.DataSet([
        { id: 1, group: 1, content: "ArcGIS Pro/ QGIS", start: "2024-01", end: "9999-09"},
        { id: 2, group: 1, content: "ML & GIS Course", start: "2024-07" },
        { id: 3, group: 2, content: "Started Flood Research", start: "2024-06" },
        { id: 4, group: 2, content: "Reservoir Optimization Study", start: "2025-03" },
        { id: 5, group: 3, content: "Won Data Challenge", start: "2025-01" },
        { id: 6, group: 3, content: "Presented at GIS Day", start: "2024-11-20" },
        { id: 7, group: 4, content: "B.Sc. in Civil Engineering at Imam Khomeini International University (IKIU), Qazvin, Iran", start: "2016-09-01", end: "2021-05-10", type:"background" },
        { id: 8, group: 4, content: "M.Sc. at Civil Engineering for Risk Mitigation, at Polytechnic University of Milan (PoliMi), Milan, Italy", start: "2021-09-01", end: "2024-04-11" , type:"background"},
        { id: 9, group: 4, content: "Research Period Studying Human Behaviour in Cascading Disasters at University of Groningen (UG), Groningen, Netherlands", start: "2024-05-01", end: "2024-08-30" , type:"background"},
        { id: 10, group: 2, content: "ArcGIS Pro", start: "2024-05-01", end: "9999-08-30", type: "range" }
        

    ]);

    // Timeline configuration options with fixed group heights
    var options = {
        groupOrder: function(a, b) { return a.value - b.value; },
        groupHeightMode: "fixed",      // Force fixed group height
        groupMinHeight: 60,            // Set minimum (and fixed) height in pixels
        stack: true,
        showCurrentTime: true,
        zoomable: false,
        horizontalScroll: true,
        moveable: true,
        wheel: { zoomSpeed: 0, deltaSpeed: 1 },
        height: "500px",
        margin: { item: 10 },
        start: "2023-01-01",
        end: "2026-12-31"
    };

    try {
        // Initialize timeline
        var timeline = new vis.Timeline(container, items, options);
        timeline.setGroups(groups);
        console.log("✅ Timeline initialized successfully!");
    } catch (error) {
        console.error("❌ Timeline creation error:", error);
        container.innerHTML = "Error loading timeline.";
    }
});
</script>
{% endraw %}