<script>
export default {
  data() {
    return {
      infos: [
        {
          img: 'email',
          subtitle: 'Email',
          text: 'pmalian@list.ru',
          href: 'mailto',
        },
        {
          img: 'link',
          subtitle: 'Website',
          text: 'https://github.com/yuKalashnikova2',
          href: 'https://github.com/yuKalashnikova2',
        },
        { img: 'location', subtitle: 'Address', text: 'Moscow, Russia' },
        { img: 'tel', subtitle: 'Phone', text: '+79858542579', href: 'tel' },
      ],
      socials: [
        {
          img: 'instagram',
          subtitle: 'Instagram',
          text: '@yuKalashnikova2',
        },
        {
          img: 'github',
          subtitle: 'Github',
          text: '@yuKalashnikova2',
        },
        {
          img: '5',
          subtitle: 'Twitter',
          text: '@yuKalashnikova2',
        },
        {
          img: 'linkedin',
          subtitle: 'Linkedin',
          text: '@yul-vilaya-965a67279',
        },
      ],
      languages: [
        { img: 'flag-1', subtitle: 'Native', text: 'Russian' },
        { img: 'flag-3', subtitle: 'Professional working', text: 'English' },
        { img: 'flag-2', subtitle: 'Elementary', text: 'Spanish' },
      ],
      hobbies: [
        { img: 'play', text: 'Gaming' },
        { img: 'earth', text: 'Traveling' },
        { img: 'brush', text: 'Sketching/Graffitti' },
        { img: 'inbox', text: 'Blogging' },
      ],
      personalDetails: [
        { subtitle: ' Olga Nikolaevna', text: 'Mother’s Name : ' },
        { subtitle: ' Lev Leontevich', text: 'Father’s Name :  ' },
        { subtitle: ' 20 - 01 - 1994', text: 'D.O.B. : ' },
      ],
    }
  },
}
</script>
<template>
  <div class="aside">
    <header class="aside__header">
      <img src="/assets/logo.png" alt="logo" class="aside__header-logo" />
      <h1 class="aside__header-title">Yuliya Kalashnikova</h1>
    </header>

    <p class="aside__about">
      Frontend - developer. Technology stack: Git; JavaScript/TypeScript, СSS,
      HTML; BEM, SASS, SCSS; Vue ( Vue3, Vue-router); Vuex, Pinia; Understanding
      of client-server architecture, experience interacting with APIs.
    </p>

    <div class="aside__main">
      <div class="aside__infos aside__block aside__block_border-gray gap-24">
        <div class="aside__infos__card" v-for="item in infos">
          <div
            class="aside__infos__card-img aside__infos__card-img_background-gray"
          >
            <img
              width="20"
              height="20"
              :src="'/assets/svg/' + item.img + '.svg'"
              :alt="item.img"
            />
          </div>

          <div class="aside__infos__card-subtitle">
            <div class="subtitle">{{ item.subtitle }}</div>
            <a
              :href="`${item.href}`"
              :class="[
                'subtitle-text',
                item.subtitle === 'Website' ? 'underline' : '',
              ]"
              >{{ item.text }}</a
            >
          </div>
        </div>
      </div>

      <div class="aside__socials aside__block aside__block_border-gray gap-20">
        <div class="subtitle">Socials</div>
        <div class="aside__infos__card" v-for="social in socials">
          <div class="aside__infos__card-img">
            <img
              :src="'/assets/svg/social/' + social.img + '.svg'"
              alt="email"
            />
          </div>

          <div class="aside__infos__card-subtitle">
            <div class="subtitle">{{ social.subtitle }}</div>
            <a :href="`${social.text}`" class="subtitle-text underline">{{
              social.text
            }}</a>
          </div>
        </div>
      </div>

      <div
        class="aside__languages aside__block aside__block_border-gray gap-20"
      >
        <div class="subtitle">Languages</div>
        <div class="aside__infos__card" v-for="language in languages">
          <div class="aside__infos__card-img">
            <img
              :src="'/assets/svg/flags/' + language.img + '.svg'"
              alt="email"
            />
          </div>

          <div class="aside__infos__card-subtitle">
            <div class="subtitle-text">{{ language.text }}</div>
            <div class="subtitle">{{ language.subtitle }}</div>
          </div>
        </div>
      </div>

      <div class="aside__hobbies gap-16">
        <div class="subtitle">Hobbies & Interests</div>
        <div class="aside__infos__card" v-for="hobbie in hobbies">
          <div class="aside__infos__card-img">
            <img
              :src="'/assets/svg/hobbies/' + hobbie.img + '.svg'"
              :alt="hobbie.img"
            />
          </div>

          <div class="aside__infos__card-subtitle">
            <div class="subtitle-text">{{ hobbie.text }}</div>
          </div>
        </div>
      </div>

      <div class="aside__personal-details gap-16">
        <div class="subtitle">Personal Details</div>
        <div class="aside__infos__card" v-for="personal in personalDetails">
          <span class="subtitle-text">{{ personal.text }} </span>

          <span class="subtitle-text subtitle-text_gray">
            {{ personal.subtitle }}</span
          >
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.aside {
  display: flex;
  flex-direction: column;
  background-color: #f7fcff;
  max-width: 355px;
  padding: 24px 4px 0 24px;
  @media (max-width: 992px) {
    max-width: 100%;
  }

  &__header {
    margin-bottom: 32px;
    @media (max-width: 992px) {
      text-align: center;
    }
    &-logo {
      border-radius: 100%;
      width: 96px;
      height: 96px;
      object-fit: cover;

      @media (max-width: 992px) {
        margin: 0 auto;
      }
    }
    &-title {
      font-size: 32px;
      font-weight: 500;
      line-height: 40px;
      letter-spacing: -2%;
      color: #2e2e48;
      padding-top: 16px;
      @media (max-width: 992px) {
        font-size: 36px;
      }
    }
  }
  &__about {
    font-size: 18px;
    font-weight: 500;
    color: #47516b;
    letter-spacing: 0.363px;
    line-height: 24px;
    padding-bottom: 10px;
    @media (max-width: 992px) {
      border-bottom: 1px solid #e2e6ee;
      padding-bottom: 20px;
      font-size: 22px;
    }
  }
  &__infos {
    &__card {
      display: flex;
      align-items: center;
      &-img {
        width: 32px;
        height: 32px;

        border-radius: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-shrink: 0;
      }
      &-subtitle {
        margin-left: 16px;
        display: flex;
        flex-direction: column;
        gap: 4px;
      }
    }
  }
  &__socials {
    border-top: 1px solid #e2e6ee;
  }
  &__hobbies {
    display: flex;
    flex-direction: column;
    @media (max-width: 992px) {
      padding-top: 10px;
      padding-bottom: 10px;
    }
  }
  &__personal-details {
    display: flex;
    flex-direction: column;
    padding-top: 32px;
    @media (max-width: 992px) {
      padding-top: 10px;
    }
  }
}

.aside__main {
  padding-right: 20px;
  padding-bottom: 30px;
  @media (max-width: 992px) {
    display: flex;
    flex-direction: column;
    gap: 30px;
  }
}
.aside__block {
  display: flex;
  flex-direction: column;

  padding-top: 32px;
  padding-bottom: 32px;
  @media (max-width: 992px) {
    padding-top: 10px;
    padding-bottom: 10px;
  }
}
.aside__infos__card-img_background-gray {
  background-color: #e2e6ee;
}
.aside__block_border-gray {
  border-top: 1px solid #e2e6ee;
}
</style>
