<template lang="pug">
  header
    b-navbar
      template(slot="brand")
        nuxt-link(class="navbar-item" to="/") 第22回 群馬高専工華祭
      template(slot="start")
        b-navbar-item(tag="nuxt-link" :to="{ path: '/greeting/' }") ごあいさつ
        b-navbar-item(tag="nuxt-link" :to="{ path: '/access/' }") アクセス
        b-navbar-item(tag="nuxt-link" :to="{ path: '/stages/list/' }") ステージ
        b-navbar-dropdown(label="企画" hoverable)
          b-navbar-item(tag="nuxt-link" :to="{ path: '/booths/list/' }") 企画一覧
          b-navbar-item(tag="nuxt-link" :to="{ path: '/booths/genre/' }") ジャンル別企画一覧
        b-navbar-item(tag="nuxt-link" :to="{ path: '/bookmark/' }") ブックマーク
      template(slot="end")
        a(class="navbar-item" href="https://twitter.com/kokasai_GNCT")
          b-icon(icon="twitter" size="is-medium")
</template>
