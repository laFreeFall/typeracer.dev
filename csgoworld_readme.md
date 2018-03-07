> It's not about design and how it looks like, it's about logic and functionality
* Frontend
* * [Vue.js](https://github.com/vuejs/vue)
* * [Axios](https://github.com/axios/axios) (ajax requests)
* * [Vue-Router](https://github.com/vuejs/vue-router) (SPA routing)
* * [Vuex](https://github.com/vuejs/vuex) (state managment)
* * [Element-UI](https://github.com/ElemeFE/element) (UI library for popups, modals, etc)
* Backend
* * [Laravel](https://github.com/laravel/laravel)
* * [Laravel Passport](https://github.com/laravel/passport) (auth)

All the screenshots and animations stored on [imgur](https://imgur.com/a/Hjhcm)
## Main Features:

* ### Cases and Collections Opening
![Opening a case](https://i.imgur.com/UfAH2m8.gif)
> There are almost 50 cases and collections available for opening. Each case contains specific rare item (knife or gloves).
Drop chances are taken from [reddit](https://www.reddit.com/r/GlobalOffensive/comments/6zd9yx/perfect_world_csgo_has_finally_published_their/).
Relative ratio between some quality and the lowest one is 1:5 except rare items (2:5 for them). Change to get a stattrak weapon is 10%.
All the items (more than 7000) were parsed from [OPSkins](https://opskins.com/) using [their API](https://opskins.com/kb/api-v2).

---

* ### Roulette
![Roulette spin](https://i.imgur.com/oFpTPWA.gif)
> Website allows to bet on all three colors per roll. Coefficients for black and red are 2, for green 14.

---

* ### Coinflip
![Coinflip](https://i.imgur.com/YdvIVA4.gif)
> User may pick up to 10 items from his inventory and try luck in a random fight with random opponent with equal bank (10% deviations in items price sum are allowed).
Winner takes all, loser gets nothing.

----

* ### Contracts
![Contract](https://i.imgur.com/mOeqDDJ.gif)
> User should pick 10 items (no less no more) with the same quality to get a weapon with better one.
Float of the received weapon will depend on average float of user`s items and it will be picked only from collections user`s items belongs to (considering rates).

---

> All the items user gets from case openings, contracts and coinflips stores in a stash - user`s inventory, where pagination and live search ara available.

![Inventory](https://image.prntscr.com/image/a-phiM2fRyKlvSR3rKDiQw.png)

---

> By clicking on the item its modal with detailed information opens allowing user to sell it for diamonds (if item worth more than $1 with ratio $1 = 1 diamond) to play using them on roulette or delete it (if item worth less than $1 you can't get any diamonds for it)

![Inventory details](https://image.prntscr.com/image/nHS7uHwUQrOKedsXrIQQYA.png)

---

> There are logs and stats accounting for each website activity including case openings, roulette spins, coinflip games and trade-up contracts.
For example, opencase stats and roulette logs are displayed below.

![Opencase statistics](https://image.prntscr.com/image/Tjh-dfQDQ76cOJMA-TpryA.png)
![Roulette stats](https://image.prntscr.com/image/z-lAnJ41QdmzNMpmluqbYQ.png)

---

> Authentication was made using Laravel Passport.

![Auth](https://i.imgur.com/z3ZVTzi.gif)

---

More screenshots are stored on [imgur album](https://imgur.com/a/Hjhcm).
