---

# Car Share Ninja

---

## What is Car Share Ninja?

- Tracks of who does what in a car share <!-- .element: class="fragment" data-fragment-index="1" -->
- Suggests who should drive next <!-- .element: class="fragment" data-fragment-index="2" -->
- Driven by a flexible and fair scoring algorithm <!-- .element: class="fragment" data-fragment-index="3" -->
- Progressive Web Application <!-- .element: class="fragment" data-fragment-index="4" -->
  - Reliable - loads instantly even with unreliable network
  - Fast - won't leave you hanging, you and your buddies have somewhere to go!
  - Engaging - feels like a natural app on device

+++

## Member Scoring System

`$$Score = \frac{DistanceAsPassenger}{DistanceAsDriver}$$`

Members with the lowest score should drive next <!-- .element: class="fragment" data-fragment-index="2" -->

+++

Ranking members by the benefit they personally recieve keeps things simple and fair.

+++

## Flexibility

Can handle: <!-- .element: class="fragment" data-fragment-index="1" -->
- holidays <!-- .element: class="fragment" data-fragment-index="1" -->
- sick days <!-- .element: class="fragment" data-fragment-index="1" -->
- differing shift patterns <!-- .element: class="fragment" data-fragment-index="1" -->
- differing distances, maybe you pick a member up on the way? <!-- .element: class="fragment" data-fragment-index="1" -->

---

# Technical Overview

+++

## API

- Stateless microservice written Go  <!-- .element: class="fragment" data-fragment-index="1" -->
- To be deployed as an autoscaling service in Kubernetes <!-- .element: class="fragment" data-fragment-index="2" -->
- Firebase JWT Authentication <!-- .element: class="fragment" data-fragment-index="3" -->
  - Library created called [firebase-jwt-auth](https://github.com/LewisWatson/firebase-jwt-auth)
- RESTful and implements JSON:API <!-- .element: class="fragment" data-fragment-index="4" -->
- MongoDB data store <!-- .element: class="fragment" data-fragment-index="5" -->

+++

## Front End

- Progressive Web Application written in Angular2  <!-- .element: class="fragment" data-fragment-index="1" -->
- Material design <!-- .element: class="fragment" data-fragment-index="2" -->
- Firebase authentication <!-- .element: class="fragment" data-fragment-index="7" -->
  - Username/Password, social, and anonymous
  - JWT token included with every API call

+++

## Progressive Web Applications

User experiences that have the reach of the web, and are reliable, fast, and engaging.

- Service workers acting as client side proxy <!-- .element: class="fragment" data-fragment-index="2" -->
  - Cache key resources to improve responsivenes
  - App takes responsibility for what happens if there is no network
- Earns it's place on users home screen, along side native apps <!-- .element: class="fragment" data-fragment-index="3" -->

---

# What is left to do?

+++

## API

- Restrict access based on user
- Sort out hosting
- Monitoring (Prometheus)

+++

## Front End

- Flesh out + polish UI <!-- .element: class="fragment" data-fragment-index="1" -->
- Add more authentication providers <!-- .element: class="fragment" data-fragment-index="1" -->
- Cache API data to fully implement Offline First <!-- .element: class="fragment" data-fragment-index="1" -->

---

## One More Thing...

+++

#### Early Preview Available

[https://carshare.ninja](https://carshare.ninja)
