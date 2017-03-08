#HSLIDE

# carshare.ninja

#HSLIDE

## What is Car Share Ninja?

- Tracks of who does what in a car share <!-- .element: class="fragment" data-fragment-index="1" -->
- Suggests who should drive next <!-- .element: class="fragment" data-fragment-index="2" -->
- Flexible while remaining fair <!-- .element: class="fragment" data-fragment-index="3" -->
- Progressive Web Application <!-- .element: class="fragment" data-fragment-index="4" -->
  - Reliable - loads instantly even with unreliable network
  - Fast - won't leave you hanging, you've got somewhere to go!
  - Engaging - feels like a native app

#HSLIDE

## Member Scoring System

`$$Score = \frac{DistanceAsPassenger}{DistanceAsDriver}$$`

Members with the lowest score should drive next <!-- .element: class="fragment" data-fragment-index="2" -->

#VSLIDE

Ranking members by the benefit they personally recieve keeps things simple and fair.

#VSLIDE

The scoring system also flexible and can handle

- holidays <!-- .element: class="fragment" data-fragment-index="1" -->
- sick days <!-- .element: class="fragment" data-fragment-index="2" -->
- differing shift patterns <!-- .element: class="fragment" data-fragment-index="3" -->
- differing distances. Maybe you pick a member up on the way? <!-- .element: class="fragment" data-fragment-index="4" -->

#HSLIDE

## Technical Overview

![Architecture Overview](images/carshare.ninja.png)

#VSLIDE

## API

- Written in Go
- Uses JSON:API
- Deployed via docker containers in Kubernetes
- Authentication via Firebase JWT tokens
- MongoDB data store

#VSLIDE

## Front End

- Written in Angular2
- Material design
- Progressive Web Application
  - Open Web
  - Service workers
  - Offline first
- Firebase authentication
  - JWT token included with every API call

#HSLIDE

# Current State

#VSLIDE

#HSLIDE

## fin
