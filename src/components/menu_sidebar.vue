<template>
  <div class="menu_sidebar">

    <Hamburger/>

    <header>
      <nav>
        <button type="button" class="hamburger_close"><span class="hamburger_line"></span></button>

        <ul>
          <li><a href="/datownik/" class="activeUrl">Main</a></li>
          <li><a href="?page=kalendarz">Kalendarz</a></li>
          <li><a href="?page=zakladki">Zakladki</a></li>
          <li><a href="?page=notatki">Notatki</a></li>
          <li><a href="?page=dokumenty">Dokumenty</a></li>
          <li><a href="?page=do-zrobienia">To do</a></li>
          <li><a href="?page=kontakty">Kontakty</a></li>
          <li><a href="?page=pliki">Pliki</a></li>
          <li><a href="?page=ustawienia">Ustawienia</a></li>
        </ul>
      </nav>
    </header>

  </div>
</template>

<script>
import Hamburger from './hamburger.vue';
export default {
  name: 'MenuSidebar',
  components: {
    Hamburger,
  },
  props: {
    // msg: String
  }
}
</script>

<style>
header {
  background-image: url('./../assets/bg_lockscreen.png');
  background-repeat:no-repeat;
  background-size: cover;
  position: fixed;
  left: 0;
  top: 0;
  bottom: 0;
  width: 320px;
  z-index: 1;
  color: #ffffff;
  font-weight: 300;
  font-size: 10px;
  overflow: hidden;
  transition: transform .2s ease;
  box-shadow: inset 0px 0px 36px -8px black;
}

header > nav {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  height: 100%;
  width: 100%;
  overflow-y: scroll;
  padding: 30px;
}

header > nav::-webkit-scrollbar {
  width: 10px;
}

header > nav::-webkit-scrollbar-track {
  -webkit-box-shadow: inset 0 0 6px rgba(0,0,0,0.3);
}

header > nav::-webkit-scrollbar-thumb {
  background-color: transparent;
  -webkit-box-shadow: inset 0 0 2px 1px rgba(255,255,255,1);
  border-radius: 2px;
}

header > nav > ul {
  display: flex;
  flex-direction: column;
  align-items: stretch;
  width: 100%;
}

header > nav > ul > li {
  font-size: 16px;
  border-bottom: 1px solid rgba(255, 255, 255, 0.15);
}

header > nav > ul > li:hover > a {
  opacity: .45;
  padding-left: 20px;
}

header > nav > ul > li > a {
  display: block;
  text-decoration: none;
  color: inherit;
  padding: 20px 0;
  transition: all .5s ease;
}

header ul li:hover a,
header ul li .active {
  /*color: #ffffff; border-color: white;*/
}

.hamburger ,
.hamburger_close {
  border: 0;
  background-color: transparent;
  padding: 0;
  outline: 0;
  cursor: pointer;
}

.hamburger:not(:hover),
.hamburger_close:not(:hover) {
  opacity: 0.8;
}

.hamburger {
  position: fixed;
  width: 32px;
  height: 22px;
  left: 10px;
  top: 22px;
  z-index: 1;
}

.hamburger > .hamburger_line,
.hamburger > .hamburger_line::before,
.hamburger > .hamburger_line::after {
  position: absolute;
  left: 0;
  background-color: #626464;
  width: 100%;
  height: 4px;
  border-radius: 1px;
  display: block;
}

.hamburger > .hamburger_line::before {
  content: '';
  top: -9px;
}
.hamburger > .hamburger_line {
  top: 50%;
  transform: translateY(-50%);
}
.hamburger > .hamburger_line::after {
  content: '';
  bottom: -9px;
}

.hamburger_close {
  position: relative;
  width: 24px;
  height: 24px;
}

.hamburger_close > .hamburger_line,
.hamburger_close > .hamburger_line::before {
  position: absolute;
  left: 0;
  background-color: white;
  width: 32px;
  height: 4px;
  border-radius: 1px;
  display: block;
}

.hamburger_close > .hamburger_line::before {
  content: '';
  top: 0;
  transform: rotate(90deg);
}
.hamburger_close > .hamburger_line {
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%) rotate(45deg);
}

/* BEFORE OPENING STYLES */
body:not(.nav_open) header {
  transform: translateX(-100%);
}

/* AFTER OPENING STYLES */
body.nav_open main {
  filter: blur(4px);
  pointer-events: none;
}
</style>
