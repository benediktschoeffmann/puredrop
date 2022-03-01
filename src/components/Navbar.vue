<template>
  <b-navbar>
    <template slot="brand">
      <b-navbar-item tag="router-link" :to="{ path: '/' }">
        <img
          src="@/assets/images/branding.png"
          alt="Lightweight UI components for Vue.js based on Bulma"
        />
      </b-navbar-item>
    </template>
    <template slot="start">

    </template>

    <template slot="end"> 
      <b-navbar-item to="/about" tag="router-link">
        About
      </b-navbar-item>
    
    </template>
  </b-navbar>
</template>
