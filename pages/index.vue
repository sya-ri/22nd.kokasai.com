<template lang="pug">
div
  Hero(title="第22回 群馬高専工華祭" subtitle="Re:Make ～平成を越えて～")
  section
    div.container
      div.columns.is-multiline.is-variable.is-2.is-light.has-text-success.has-text-centered
        div.column.is-full
          Timer
        div.column.is-one-third
          article.title.is-child.notification.is-light.has-text-success.has-text-centered
           div.content
            b-icon(icon="textbox" size="is-large")
            p.is-size-3-mobile.is-size-2-desktop.has-text-weight-semibold 名称
            p.is-size-4-mobile.is-size-4-desktop.has-text-weight-light 第22回 群馬高専工華祭
        div.column.is-one-third
          article.title.is-child.notification.is-light.has-text-success.has-text-centered
           div.content
            b-icon(icon="clock" size="is-large")
            p.is-size-3-mobile.is-size-2-desktop.has-text-weight-semibold 日時
            p.is-size-4-mobile.is-size-4-desktop.has-text-weight-light 2019/11/02(土)~2019/11/03(日)
            p.is-size-4-mobile.is-size-4-desktop.has-text-weight-light 両日 09:30~16:30
        div.column.is-one-third
          article.title.is-child.notification.is-light.has-text-success.has-text-centered
           div.content
            b-icon(icon="clipboard-outline" size="is-large")
            p(class="is-size-3-mobile is-size-2-desktop has-text-weight-semibold") テーマ
            p(class="is-size-4-mobile is-size-4-desktop has-text-weight-light") "Re:make ~平成を越えて~"
        div.column.is-one-third
          article.title.is-child.notification.is-light.has-text-success.has-text-centered
           div.content
            span.icon.is-large
              i.mdi.mdi-map-marker
            p(class="is-size-3-mobile is-size-2-desktop has-text-weight-semibold") 場所
            p(class="is-size-4-mobile is-size-4-desktop has-text-weight-light")
              nuxt-link(to="/access/") 群馬工業高等専門学校
        div.column.is-one-third
          article.title.is-child.notification.is-light.has-text-success.has-text-centered
           div.content
            b-icon(icon="account" size="is-large")
            p(class="is-size-3-mobile is-size-2-desktop has-text-weight-semibold") 主催
            p(class="is-size-4-mobile is-size-4-desktop has-text-weight-light") 第22回 群馬高専工華祭実行委員会
</template>

<script>
import Hero from '@/components/Hero.vue';
import Meta from "~/assets/mixins/meta";
import Timer from "@/components/Timer.vue";

export default {
  mixins:[
    Meta
  ],
  components: {
    Hero,
    Timer
  },
  data() {
    return {
      titleTemplate: null,
    }
  },
  head() {
    return {
      title: "トップ",
      meta: [
        { charset: 'utf-8' },
        { name: 'viewport', content: 'width=device-width, initial-scale=1' },
        { hid: 'description', name: 'description', content: "2019/11/02~2019/11/03に開催する第22回群馬高専工華祭の公式Webサイトです。" },
        { hid: "og:title", property: "og:title", content: "第22回 群馬高専工華祭"},
        { hid: "og:type", property: "og:type", content: "website"},
        { hid: "og:url", property: "og:url", content: "https://22nd.kokasai.com/"},
        { hid: "og:description", property: "og:description", content: "2019/11/02~2019/11/03に開催する第22回群馬高専工華祭の公式Webサイトです。"},
        { hid: "og:email", property: "og:email", content: "kokasai.gnct@gmail.com"},
        { hid: "og:site_name", property: "og:site_name", content: "群馬高専工華祭実行委員会 公式サイト"},
        { hid: "og:locale", property: "og:locale", content: "ja_JP"},
        { hid: "og:image", property: "og:image", content: "/logo.png"},
        { name: "twitter:card", content: "summary"},
        { name: "twitter:site", content: "@kokasai_GNCT"},
        { name: "twitter:url", content: "https://22nd.kokasai.com/"},
        { name: "twitter:title", content: "トップ - 第22回 群馬高専工華祭"},
        { name: "twitter:description", content: "2019/11/02~2019/11/03に開催する第22回群馬高専工華祭の公式Webサイトです。"},
        { name: "twitter:image", content: "/logo.png"}
      ],
      script: [
        {
          type: "application/ld+json",
          innerHTML: JSON.stringify({
            "@context": "https://schema.org/",
            "@graph": [
              {
                "@id": "https://kokasai.com/#organization",
                "@type": "Organization",
                "name": "群馬工業高等専門学校 工華祭実行委員会",
                "url": [
                    "https://kokasai.com/",
                    "https://twitter.com/kokasai_GNCT"
                ]
              },
              {
                "@id": "https://kokasai.com/#website",
                "@type": "WebSite",
                "url": "https://kokasai.com/",
                "name": "群馬高専 工華祭実行委員会 ホームページ",
                "keywords": "群馬高専,群馬工業高等専門学校,National Institute of Technology Gunma College,NITGC,文化祭,工華祭,kokasai",
                "isPartOf": {
                    "@id": "https://kokasai.com/#website"
                },
                "publisher": {
                    "@id": "https://kokasai.com/#organization"
                },
                "sameAs": "https://twitter.com/kokasai_GNCT"
              },
              {
                "@id": "https://22nd.kokasai.com/#toppage",
                "@type": "WebPage",
                "url": "https://22nd.kokasai.com/",
                "name": "第22回 群馬高専工華祭 ホームページ",
                "isPartOf": {
                    "@id": "https://kokasai.com/#website"
                },
                "inLanguage": "ja",
                "keywords": "群馬高専,群馬工業高等専門学校,National Institute of Technology Gunma College,NITGC,文化祭,工華祭 2019,第22回 工華祭,kokasai",
                "publisher": {
                    "@id": "https://kokasai.com/#organization"
                },
                "copyrightHolder": {
                    "@id": "https://kokasai.com/#organization"
                },
                "copyrightYear": 2019,
                "publication": {
                    "@id": "https://22nd.kokasai.com/#event"
                }
              },
              {
                "@id": "https://22nd.kokasai.com/#event",
                "@type": "PublicationEvent",
                "name": "第22回 群馬高専工華祭",
                "isAccessibleForFree": true,
                "inLanguage": "ja",
                "location": {
                    "@type": "PostalAddress",
                    "@language": "ja",
                    "addressCountry": "日本",
                    "addressRegion": "群馬県",
                    "addressLocality": "前橋市",
                    "streetAddress": "鳥羽町580番地"
                },
                "organizer": {
                    "@id": "https://kokasai.com/#organization"
                },
                "startDate": [
                    "2019-11-02T09:00:00Z+09:00",
                    "2019-11-03T09:00:00Z+09:00"
                ],
                "endDate": [
                    "2019-11-03T18:00:00Z+09:00",
                    "2019-11-02T18:00:00Z+09:00"
                ]
              }
            ]
          })
        }
      ],
      __dangerouslyDisableSanitizers: ["script"]
    }
  }
}
</script>

