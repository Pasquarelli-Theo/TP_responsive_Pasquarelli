
<template>
  <section class="bg-indigo-50">
          <header
      class="
        sticky
        top-0
        z-40
        h-16
        w-full
        border-b border-b-indigo-100
        bg-gray-100
        px-3
      "
    >
      <div class="flex h-full w-full items-center justify-between">
        <div class="flex items-center">
          <HomeIcon class="w-8 fill-indigo-500" />
          <span class="font-semibold">Estatery</span>
        </div>
        <div class="lg:hidden">
          <MenuIcon class="w-8 cursor-pointer" @click="MenuOpen = !MenuOpen" />
        </div>
        <nav
          class="
            absolute
            left-0
            top-16
            w-full
            -translate-y-[200%]
            bg-slate-300
            pl-2
            lg:relative lg:top-0 lg:w-fit lg:translate-y-0 lg:bg-transparent
          "
          :class="MenuOpen && 'translate-y-0'"
        >
          <ul class="flex flex-col gap-8 py-4 font-bold lg:flex-row">
            <li>Rent</li>
            <li>Buy</li>
            <li>Sell</li>
            <li>Manage Property</li>
            <li>Ressources</li>
          </ul>
        </nav>
        <div class="menu-text gap-4">
          <button class="bouton2 mt-1 mb-1 font-bold text-[#6366F1]">
            Login
          </button>
          <button class="bouton1 mr-2 mt-1 mb-1 font-bold text-white">
            Sign Up
          </button>
        </div>
      </div>
    </header>
      <main>
        <h2 class="text-lg font-bold text-center mb-4">Search proprieties to rent</h2>
        <section class="overflow-hidden flex items-center justify-center ">
          <div class="pt-2 relative mx-auto text-gray-600">
            <input class="border-2 border-gray-300 bg-white h-10 px-5 pr-16 rounded-lg text-sm focus:outline-none"
              type="search" name="search" placeholder="Search location">
            <button type="submit" class="absolute right-0 top-0 mt-5 mr-4">
              <svg class="text-gray-600 h-4 w-4 fill-current" xmlns="http://www.w3.org/2000/svg"
                xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" id="Capa_1" x="0px" y="0px"
                viewBox="0 0 56.966 56.966" style="enable-background:new 0 0 56.966 56.966;" xml:space="preserve"
                width="512px" height="512px">
                <path
                  d="M55.146,51.887L41.588,37.786c3.486-4.144,5.396-9.358,5.396-14.786c0-12.682-10.318-23-23-23s-23,10.318-23,23  s10.318,23,23,23c4.761,0,9.298-1.436,13.177-4.162l13.661,14.208c0.571,0.593,1.339,0.92,2.162,0.92  c0.779,0,1.518-0.297,2.079-0.837C56.255,54.982,56.293,53.08,55.146,51.887z M23.984,6c9.374,0,17,7.626,17,17s-7.626,17-17,17  s-17-7.626-17-17S14.61,6,23.984,6z" />
              </svg>
            </button>
          </div>
        </section>
        <section>
        </section>
        
        <div class="grid grid-flow-row-dense grid-cols-[repeat(auto-fit,minmax(400px,1fr))]">
            <card 
              :nbrbath="1"
              :nbrbed="4"
              :price="2800"
              :favori="false"
              image="/images-maisons/maison-1.jpg"
              location="Beverly Springfield"
              size="6x75²"
              adress="(256) 574-4323
                      1265 King St
                      Midland City, Alabama(AL), 36350"/>
            <card 
              :nbrbath="2"
              :nbrbed="5"
              :price="5000"
              :favori="true"
              image="/images-maisons/maison-2.jpg"
              location="Nowhere Town"
              size="240m²"
              adress="(256) 632-2378
                      1263 County Rd #295
                      Higdon, Alabama(AL), 35979"/>
          </div>
          <div class="text-center my-10">
            <ChevronLeftIcon class="inline-block text-right w-8"/>
            <p class="inline-block ml-4 mr-4 text-base text-white bg-indigo-900 py-2 px-4 rounded-full ">1</p>
            <p class="inline-block ml-4 mr-4 text-base text-indigo-900 bg-White py-2 px-4 rounded-full ">2</p>
            <p class="inline-block ml-4 mr-4 text-base text-indigo-900 py-2 px-5 ">...</p>
            <p class="inline-block ml-4 mr-4 text-base text-indigo-900 bg-White py-2 px-3 rounded-full ">10</p>
            <ChevronRightIcon class="inline-block text-right w-8"/>
          </div>
      </main>
      <footer class="p-3 mt-5 mb-5 bg-gray-50">
          <MailOpenIcon class="inline-block w-10"/>
          <p class="inline-block ml-4 mr-4 text-lg text-blue-600 ">Estatery</p>
        <div class="grid grid-rows-3 grid-flow-col">
          <div class="m-5">
            <h3 class="font-bold mb-2">SELL A HOME</h3>
            <p>Request an offer</p>
            <p>Pricing</p>
            <p>Reviews</p>
            <p>Stories</p>
          </div>
          <div class="m-5">
            <h3 class="font-bold mb-2">BUY A HOME</h3>
            <p>Buy</p>
            <p>Finance</p>
          </div>
          <div class="m-5">
            <h3 class="font-bold mb-2">BUY, RENT AND SELL</h3>
            <p>Buy & sell proprieties</p>
            <p>Rent home</p>
            <p>Builder trade-up</p>
          </div>
          <div class="m-5">
            <h3 class="font-bold mb-2">TERMS &  PRIVACY</h3>
            <p>Trust & Safety</p>
            <p>Terms of Service</p>
            <p>Privacy Policy</p>
          </div>
          <div class="m-5">
            <h3 class="font-bold mb-2">ABOUT</h3>
            <p>Company</p>
            <p>How it works</p>
            <p>Contact</p>
            <p>Invertors</p>
          </div>
          <div class="m-5">
            <h3 class="font-bold mb-2">RESSOURCES</h3>
            <p>Blog</p>
            <p>Guides</p>
            <p>FAQ</p>
            <p>Help Center</p>
          </div>
        </div>
        <hr> <hr>

        <div class="text-center my-5">
          <p class="text-sm text-gray-400">2021 Estatery. All rights reserved</p>
          <AtSymbolIcon class="inline-block w-5 m-3"/>
          <QuestionMarkCircleIcon class="inline-block w-5 m-3"/>
          <ChatAltIcon class="inline-block w-5 m-3"/>
          <GiftIcon class="inline-block w-5 m-3"/>
        </div>

      </footer>
  </section>
    <br>
</template>
<style >
.bouton1 {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 12px 24px;
  background: #6366f1;
  border-radius: 8px;
}
.bouton2 {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 10px 22px;
  border: 2px solid #c7d2fe;
  border-radius: 8px;
}
.menu {
  display: block;
}
.menu-text {
  display: none;
  align-items: center;
}
/** média **/
@media screen and (min-width: 1024px) {
  .menu {
    display: none;
  }
  .menu-text {
    display: flex;
  }
}
</style>
<script>
import card from "./components/card.vue";
import { HomeIcon } from "@heroicons/vue/solid";
import { MenuIcon, ChevronDownIcon, SearchIcon } from "@heroicons/vue/outline";
import bouton from "./components/bouton.vue";
import { ArchiveIcon, BellIcon, AdjustmentsIcon, UserAddIcon, ChatIcon, MailOpenIcon, MenuAlt4Icon, ChevronRightIcon, ChevronLeftIcon, AtSymbolIcon, QuestionMarkCircleIcon, ChatAltIcon, GiftIcon } from "@heroicons/vue/outline";
export default {
  name: "App",
  components: { 
  card, 
  bouton, 
  HomeIcon, 
  MenuIcon, 
  ChevronDownIcon, 
  SearchIcon, 
  ArchiveIcon, 
  BellIcon, 
  AdjustmentsIcon, 
  UserAddIcon, 
  ChatIcon, 
  MailOpenIcon, 
  MenuAlt4Icon, 
  ChevronRightIcon, 
  ChevronLeftIcon, 
  AtSymbolIcon, 
  QuestionMarkCircleIcon, 
  ChatAltIcon, 
  GiftIcon },
  
    data() {
    return {
      MenuOpen: false,
    };
  },
};
</script>


