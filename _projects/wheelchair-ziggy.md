---
layout: project
title: "Modified wheelchair to facilitate pushing from the side"
date: 2024-09-12
summary: This patented wheelchair modification allows the caregiver to push the wheelchair while walking beside the occupant without additional effort.
tags: rehabilitation, vehicle dynamics
status: "Published"
collaborators:
   - "Matto Leeuwis"
   - "Job Sesink"
   - "Lucy Bennett"
   - "Emma Schippers"
   - "Marieke Vassen"
   - "Katie Poggensee"
   - "Heike Vallery"
image: /assets/projects/ziggy-thumb.jpg   # path to the thumbnail
image_alt: Wheelchair pushed from the side                # optional
\# code: https://github.com/USER/REPO            # (add if/when public)
link: https://doi.org/10.1371/journal.pone.0307759
---
Traditional wheelchairs are pushed from behind the occupant, which hinders eye contact and communication. It was proposed that the wheelchair be pushed from the side using a push bar to place the caregiver beside the occupant. However, this method requires the caregiver to exert continuous effort to maintain a straight trajectory because the force at the lateral push location generates a moment. This study explores simple modifications to the front castor wheel of the wheelchair that allow pushing it from the side without additional effort. We used a three-dimensional dynamic model of the castor wheel to predict the effects of altering its dimensions and rake, cant, and bank angle and present a simplified steady-state solution. Experimental results support the model's predictions, and a proof-of-concept experiment with a wheelchair showed that it is possible to push a wheelchair from the side without increasing forces or moments. The results also confirmed that the lateral ground reaction force generated on the castor wheel is proportional to the normal force and the cant angle, which can counter the moment caused by the lateral push location. The implications of this model extend beyond wheelchair design and can be applied to other applications that use castor wheels, such as robotics, trolleys, and walkers.

<figure>
  <video controls preload="metadata" playsinline
         src="{{ '/assets/projects/ziggy-S3-video.mp4' | relative_url }}"
         type="video/mp4" style="max-width:100%; height:auto;">
    Your browser can’t play this video.
    <a href="{{ '/assets/projects/ziggy-S3-video.mp4' | relative_url }}">Download MP4</a>.
  </video>
  <figcaption>Wheelchair being pushed from the side</figcaption>
</figure>

## Thesis
During my MSc thesis I developed a multibody dynamic model of the wheelchair to simulate how our modification of the castor wheel affected the system. We found that the cant (i.e., slant or tilt) of the swivel axis proportionally increased the lateral force it generates. This lateral force turns the wheelchair to one side. By letting the caregiver push using a lateral extending bar the wheelchair moves in a straight line. The thesis contains a simulation of a whole wheelchair to estimate the curvature of trajectories given the parameters of the wheelchair and castor wheel. The publication simplified the representation by validating the dynamics of the castor wheel itself.

MSc thesis: [The Dynamics of Non-upright Castor Wheels and Their Application for Pushing Wheelchairs from the Side](https://resolver.tudelft.nl/uuid:40db5c5a-225d-44c9-9447-93b7ccffac88)

![Overview of wheelchair castor wheel](/assets/projects/wheelchair-castor-wheel-overview.svg)

## Ziggy mobility
This project led to the formation of Ziggy Mobility by Lucy Bennett and Job Sesink. Ziggy Mobility aims to bring a wheelchair to the market.

Ziggy Mobility: [Website](https://www.ziggy-mobility.nl/) | [LinkedIn](https://www.linkedin.com/company/ziggy-mobility/)

Patent: [Wheelchair](https://worldwide.espacenet.com/patent/search/family/084331279/publication/NL2033392B1?q=pn%3DNL2033392B1)
