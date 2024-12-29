---
published: false
category: project
project_category: Flying Better
project_name: Understanding MacCready for Paraglider Pilots
date: 2024-12-28T12:56:24-08:00
title: Understanding MacCready for Paraglider Pilots
cover_photo: /content/projects/Flying_Better/Understanding_MacCready_for_Paraglider_Pilots/photos/cover_photo.jpg
layout: project-post
---

## Understanding MacCready for Paraglider Pilots
2024-12-28

## Introduction
Dr. Paul MacCready was a prolific aeronautical engineer, known for [winning the Kremer prize for human powered aircaft](https://en.wikipedia.org/wiki/MacCready_Gossamer_Condor), wining the US sailplane nationals in 1948, 1949, and 1953, and starting the UAS company [Aerovironment](https://www.avinc.com/). MacReady speed to fly theory, invented by and named after Dr. MacCready, is a concept one may come across in any soaring sport (sailplanes, paragliders, etc). 

MacCready theory seeks to answer a simple question: When a pilot is at the top of a thermal in a non-powered aircraft, how fast should the pilot fly to the next thermal?

As non-powered aircraft fly faster, their sink rate drops off non-linearly. One way to think of this is that glide ratio, the distance flown horizontally divided by the altitude lost, decreases with additional speed. For example, on a EN-B paraglider, one may fly at 10:1 at 38km/h (trim), but this drops non-linearly to ~7:1 at ~52km/h (full speed bar). 

The bounding of the MacCready problem is relatively simple- knowing this relationship for a glider and the known strength of the next climb the pilot will take, minimize the sum of the time spent gliding and the time spend climbing by optimizing the speed that the pilot will fly between thermals.

{%- include photo.html 
    path="photos/MCDiagram.png"
    style = "width:80%;"
-%}.

## Brief MacCready Solution Derivation

Here's a brief derivation of MacCready speed to fly. 

Let's first state our objective.

$Minimize: t_{total}(V_{Horizontal}) = t_{Flying} + t_{Climbing}$
$t_{Flying}=D_{Horizontal}/V_{horizontal}$
$t_{Climbing}=\frac{Alt_{Lost}}{V_{Climb}}$
Where :
$D_{horizontal}$  : distance between climbs

$V_{horizontal}$   : horizontal velocity

$V_{climb}$  : expected vertical velocity of the next climb

$Alt_{Lost}$ is the altitude lost flying between the thermals, based on our horizontal speed:

$Alt_{Lost}=t_{Flying}*SinkRate(V_{horizontal})$

Substituting everything back into the objective and doing some simplification:

$Min:  t_{total} = t_{Flying} + \frac{t_{Flying}*SinkRate(V_{horizontal)}}{V_{Climb}}$

 $Min: t_{total} = t_{Flying} (1 + \frac{ SinkRate(V_{horizontal})}{ V_{Climb}})$
 
$Min:  t_{total} = \frac{D_{Horizontal}}{V_{Climb}} * ( \frac{V_{Climb} + SinkRate(V_{horizontal})}{V_{horizontal}})$

$D_{horizontal}$ and $V_{Climb}$ are constants, so they can be factored out, yielding:

$Min:  t_{total} =  \frac{V_{Climb} + SinkRate(V_{horizontal})}{V_{horizontal}}$

We can solve this by differentiating with respect to $V_{horizontal}$  and finding the intercept:

$0 = (\frac{V_{Climb} + SinkRate(V_{horizontal})}{V_{horizontal}})\frac{d}{dV_{Horizontal}}$

$0 = \frac{SinkRate'(V_{Horizontal})}{V_{Horizontal}} - \frac{V_{Climb} + SinkRate(V_{horizontal})}{V_{horizontal}^2}$

$\frac{SinkRate'(V_{Horizontal})}{V_{Horizontal}} = \frac{V_{Climb} + SinkRate(V_{horizontal})}{V_{horizontal}^2}$

$V_{Climb} + SinkRate(V_{horizontal}) = V_{Horizontal} * SinkRate'(V_{Horizontal})$

This is equivalent to [MacCready's equation](https://soaringweb.org/Soaring_Index/1954/PDF/1954_Mar-Apr_08.html), first published in *Soaring* Magazine, Mar-Apr 1954 issue. 

This is likely best interpreted visually on the polar graph:
{%- include photo.html 
    path="photos/PolarChart.png"
    style = "width:30%;"
-%}.

## MacCready Interpretation

### Strict MacCready doesn't work.
Wha situations break MacCready? Every one. 

### MacCready as a tool


## How to get better at determining true MacCready Number



## MacCready Flight Modes



{%- include photo.html 
    path="photos/tranparent_chart.png"
    style = "width:80%;"
-%}.

### MC 0.5
### MC 1
### MC 2
### MC 3

### Bonus: Gliding in wind, 

## Extra



Write about your project progress here!

- Add photos to the *content/projects/Flying_Better/Understanding_MacCready_for_Paraglider_Pilots/photos* folder
- Add a single cover photo as cover_photo.jpg



