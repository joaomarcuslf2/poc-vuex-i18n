<template>
  <nav id="navbar" class="navbar is-fixed-top is-dark">
    <div class="navbar-brand">
      <a class="navbar-item">
        <h2 class="subtitle has-text-centered">
          {{ $t("message.hello") }} <a href="https://github.com/joaomarcuslf">@joaomarcuslf</a>
        </h2>
      </a>

      <div class="navbar-burger burger" data-target="navMenu" @click="showNav = !showNav" :class="{ 'is-active': showNav }">
        <span></span>
        <span></span>
        <span></span>
      </div>
    </div>

    <div id="navMenu" class="navbar-menu" :class="{ 'is-active': showNav }" @click="showNav = !showNav">
      <div class="navbar-end">
        <div class="navbar-item is-fullwidth">
          <LanguageChanger />
        </div>

        <Navlink
          path="/"
          v-bind:text="$t('button.index')"
        />

        <Navlink
          path="/states"
          v-bind:text="$t('button.states')"
        />
      </div>
    </div>
  </nav>
</template>

<script src="./Navbar.js" />
<style src="./Navbar.css" />
