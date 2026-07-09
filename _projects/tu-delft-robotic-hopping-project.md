---
layout: project
title: "Robohopper"
date: "2017-01-01"
summary: A hopping robot built developed as the first-year mechanical engineering BSc capstone project at TU Delft.
tags: [robotics, mechanical engineering, education]
status: "Complete"
collaborators:
   - "Group project"
image: /assets/projects/robohopper-thumb.png 
image_alt: Robohopper jumping robot
# code: 
---
Final project of the first year of the Mechanical Engineering BSc at TU Delft. The goal was to build a one-legged jumping robot that could race to the finish, inspired by [Raibert's hopping robots from the 1980s](https://www.youtube.com/watch?v=Bd5iEke6UlE).

<figure>
  <video controls preload="metadata" playsinline
         src="{{ '/assets/projects/robohopper-demonstration-cropped.mp4' | relative_url }}"
         type="video/mp4" style="max-width:100%; height:auto;">
    Your browser can't play this video.
    <a href="{{ '/assets/projects/robohopper-demonstration-cropped.mp4' | relative_url }}">Download MP4</a>.
  </video>
  <figcaption>Robohopper jumping during one of the early tests</figcaption>
</figure>

The robohopper uses the inertia of the body to pitch itself up for the launch forward. You may also notice that there were no industrial design students in our team, which can be inferred from the complete lack of user friendliness. During the competition, it scored 4th place with a distance of 38 meter in 5 minutes on the [Delft market square](https://en.wikipedia.org/wiki/Delft_tower_experiment).

![Robohopper CAD render](/assets/projects/robohopper-cad-detail.png)

The design uses a snail cam to build up energy for a jump. Interestingly, and completely coincidentally, this is the same mechanism that was used for our <a href="{{ '/projects/inspiration-covid-mechanical-ventilator/' | relative_url }}">mechanical ventilator project</a>. 

![Robohopper CAD render](/assets/projects/robohopper-cad-detail-2.png)

I now use this project as a teaching example in my lectures in the NeuroRobotics course, where we discuss how complex movements can emerge from simple systems and controllers. Biological walking, and jumping for that matter, appear hopelessly complex to control at first. By deconstructing movement from the simple controllers of Raibert's system, the lack of controller in this Robohopper, or even the complete lack of any actuation at all (like the passive dynamic walker below), we can demonstrate that simple (neural) embeddings allow complex movements to emerge.

<figure>
  <video controls preload="metadata" playsinline
         src="{{ '/assets/projects/passive-walker-cropped.mp4' | relative_url }}"
         type="video/mp4" style="max-width:100%; height:auto;">
    Your browser can't play this video.
    <a href="{{ '/assets/projects/passive-walker-cropped.mp4' | relative_url }}">Download MP4</a>.
  </video>
  <figcaption>Tripping passive walker, assembled during Dynamic Walking 2025</figcaption>
</figure>

