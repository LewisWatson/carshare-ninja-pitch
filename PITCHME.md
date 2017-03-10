---

# carshare.ninja

---

## What is carshare.ninja?

- Tracks who does what in a car share <!-- .element: class="fragment" data-fragment-index="1" -->
- Suggests who should drive next <!-- .element: class="fragment" data-fragment-index="2" -->
- Driven by a flexible and fair scoring algorithm <!-- .element: class="fragment" data-fragment-index="3" -->
- Progressive Web Application <!-- .element: class="fragment" data-fragment-index="4" -->
  - Reliable - loads instantly even with unreliable network
  - Fast - won't leave you hanging, you and your buddies have somewhere to go!
  - Engaging - feels like a natural app on device

---

## Member Scoring System

`$$Score = \frac{DistanceAsPassenger}{DistanceAsDriver}$$`

Members with the highest score should drive next <!-- .element: class="fragment" data-fragment-index="2" -->

---

Ranking members by the benefit they personally recieve keeps things simple and fair.

---

## Flexibility

- holidays 
- sick days 
- differing shift patterns 
- differing distances, maybe you pick a member up on the way?

##### All gracefully handled

---

# Technical Overview

---

## API

- Uses [Kubernetes](https://kubernetes.io/) for automated deployment, scaling and management
- Containerised, stateless, microservice written [Go](https://golang.org)
- [Firebase JWT Authentication](https://firebase.google.com/docs/auth/admin/verify-id-tokens#verify_id_tokens_using_a_third-party_jwt_library) 
  - Currently no official Go library, so created one called [firebase-jwt-auth](https://github.com/LewisWatson/firebase-jwt-auth)
- RESTful and implements [JSON:API](http://jsonapi.org/) 
- [MongoDB](https://www.mongodb.com/) data store

---

## Front End

- [Progressive Web Application](https://developers.google.com/web/progressive-web-apps/) written in [Angular2](https://angular.io/)
- Uses [Material design](https://material.io/guidelines/material-design/introduction.html)
- [Firebase authentication](https://firebase.google.com/docs/auth/)
  - Uses official Angular2 library [AngularFire2](https://github.com/angular/angularfire2)
  - Username/Password, social, and anonymous
  - [JWT](https://jwt.io) token included with every API call

---

#### Early Preview

[https://carshare.ninja](https://carshare.ninja)

##### Source Code

https://github.com/LewisWatson/carshare-angular2/
https://github.com/LewisWatson/carshare-back/
http://gopkg.in/LewisWatson/firebase-jwt-auth.v1