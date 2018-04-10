> It's not about design and how it looks like, it's about logic and functionality
* Frontend
* * [Vue.js](https://github.com/vuejs/vue)
* * [Axios](https://github.com/axios/axios) (ajax requests)
* * [Vue-Router](https://github.com/vuejs/vue-router) (SPA routing)
* * [Vuex](https://github.com/vuejs/vuex) (state managment)
* * [Normalizr](https://github.com/paularmstrong/normalizr) (for normalizing nested 1:M Game:Key entities on frontend)
* * [Vuex-loading](https://github.com/f/vuex-loading) (for watching on state loading)
* * [Vue-select](https://github.com/sagalbot/vue-select) (for smart select fetching options from server while typing)
* * [Vue-toasted](https://github.com/shakee93/vue-toasted) (for displaying toast messages after ajax responses)
* * [V-tooltip](https://github.com/Akryum/v-tooltip) (for displaying tooltpips on keys hovering)
* * [V-click-outside](https://github.com/ndelvalle/v-click-outside) (for hiding header block via clicking outside it)
* * [Vue-content-loading](https://github.com/LucasLeandro1204/vue-content-loading) (for displaying loading cards while fetching data)

* Backend
* * [Laravel](https://github.com/laravel/laravel)
* * [Laravel Passport](https://github.com/laravel/passport) (auth)

KeysStash will help you to manage game keys. If you have ones which you haven't activated but want to store them for the near future - this is definitely your choice! Here you can easily store and manage your keys.

All the screenshots and animations stored on [imgur](https://imgur.com/a/nnaZG)

## Main Features:

* ### Keys Stash Filtering
![Keys filtering](https://i.imgur.com/M1s5kFj.gif)

* * Initially [Vuex-loading](https://github.com/f/vuex-loading) detects that keys are loading and display [Vue-content-loading](https://github.com/LucasLeandro1204/vue-content-loading) cards. After receiving nested keys and games from server [normalizr](https://github.com/paularmstrong/normalizr) normalizing them for comfortable future managing. Vue.js displays each Game with its keys in a single Card (masonry-like [Bootstrap-4 Card-Column component](https://getbootstrap.com/docs/4.0/components/card/#card-columns)). If a game doesn't have keys, its image became gray and card-header background changes from blue 'info' to gray 'light' to show that it's inactive.
* * You can filter keys by their status (are they used or not). It's very helpfull not to get confused with both used and non-used keys.
* * Filtering 'Steam'/'Non-Steam' allows you to switch games distributive platform. Game counts as Steam if it has Steam ID which is filling automatically when you're typing Game Title while adding a new game.
* * Sorting by different categories helps you to display first new/old games, games with the biggest amount of keys or just sorted in alphabetical order
* * You can also just start type game name on the top search field and all the games will be filtered using your name.

---

* ### Adding new keys and toggling existing ones
![Keys storing and toggling](https://i.imgur.com/lqbav4X.gif)

* * If you want to add a key, just start typing it in the input below needed game card. Website will show you if you're doing right or not via displaying little tip below the input. Different games distributing platforms have different key templates. For example, Steam keys always looks like 123AB-324SC-SCJ82, so they should contain three pairs of capital letters and digits concatenated by hyphen. So, when you are adding a key to a Steam game, we validate it via regexp following to exactly this pattern. If you add Non-Steam game, validation rules changes.
* * If you want to activate a key - click on a copy button on the right side, the key will be copied to your clipboard. After redeeming check it as used via clicking on a circle icon on the left side. Key will be immediately removed from the 'new' tab and will be placed to 'used' one.
* * If you're confused with a lot of game cards and want to work only with one of them - click on its title or image and you'll be redirected to single game page - where only selected game will displayed. It will be more wider and all the keys will be displayed without spoilers (on the home page if a game has more then 5 keys, others will be hidden by default).

* ### Adding new game
![Adding new game](https://i.imgur.com/VL2RNj0.gif)

* * If you wanted to add a key but haven't found its Game on our website, you can add a new one!
* * If the Game is located on Steam Store, you just should start typing its title in the first input. Website automatically will update select's options and offer you filtered by your request games. After your choice all inputs below will be filled for you. Website detects game Steam ID and creates game Steam link and image based on it.
* * If the Game was located on Steam Store, but you can't find it via our instant search while trying to add - click on the checkbox below the input and you'll be able to type full game title without our help. In most cases it happens because Steam often break relations with some game developers and deletes their games from the Store. That's why it's not stored in our database more and you can't find it instantly.
* * If the Game is distributed not by Steam, you can toggle the Switch above and the form'll change. Only two fields needed for Non-Steam games are Title and Image, and the second one is not necessary.


---

More screenshots are stored on [imgur album](https://imgur.com/a/nnaZG).
