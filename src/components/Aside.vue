<script>
export default {
  data() {
    return {
      infos: [
        {
          img: 'email',
          subtitle: 'Email',
          text: 'pmalian@list.ru',
        },
        {
          img: 'link',
          subtitle: 'Website',
          text: 'https://github.com/yuKalashnikova2',
        },
        { img: 'location', subtitle: 'Address', text: 'Moscow, Russia' },
        { img: 'phone', subtitle: 'Phone', text: '+79855679856' },
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
          img: 'li',
          subtitle: 'Linkedin',
          text: '@yul-vilaya-965a67279',
        },
      ],
    }
  },
}
</script>
<template>
  <div class="aside">
    <header class="aside__header">
      <img src="../assets/logo.png" alt="logo" class="aside__header-logo" />
      <h1 class="aside__header-title">Yuliya Kalashnikova</h1>
    </header>

    <p class="aside__about">
      A well-organized, creative and goaloriented graduate possessing excellent
      communication, problem-solving and leadership skills with a flair to
      explore Computer Science Engineering
    </p>

    <div class="aside__main">
      <div class="aside__infos aside__block gap-12">
        <div class="aside__infos__card" v-for="item in infos">
          <div class="aside__infos__card-img">
            <img
              :src="'src/assets/svg/' + item.img + '.svg'"
              alt="email"
              width="10"
              height="10"
            />
          </div>

          <div class="aside__infos__card-subtitle">
            <div class="subtitle">{{ item.subtitle }}</div>
            <a
              :href="`${item.text}`"
              :class="[
                'subtitle-text',
                item.subtitle === 'Website' ? 'underline' : '',
              ]"
              >{{ item.text }}</a
            >
          </div>
        </div>
      </div>

      <div class="aside__socials aside__block gap-10">
        <div class="subtitle">Socials</div>
        <div class="aside__infos__card" v-for="social in socials">
          <div class="aside__infos__card-img">
            <img
              :src="'src/assets/svg/social/' + social.img + '.svg'"
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
    </div>
  </div>
</template>

<style lang="scss">
.aside {
  display: flex;
  flex-direction: column;
  background-color: #f7fcff;
  width: 176px;
  padding: 24px 4px 0 24px;

  &__header {
    margin-bottom: 16px;
    &-logo {
      border-radius: 100%;
      width: 48px;
      height: 48px;
    }
    &-title {
      font-size: 16px;
      font-weight: 500;
      line-height: 20px;
      letter-spacing: -2%;
      color: #2e2e48;
      padding-top: 8px;
    }
  }
  &__about {
    font-size: 9px;
    font-weight: 500;
    color: #47516b;
    letter-spacing: 2%;
    line-height: 12px;
    padding-bottom: 5px;
  }
  &__infos {
    &__card {
      display: flex;
      word-break: break-all;
      &-img {
        width: 16px;
        height: 16px;
        background-color: #e2e6ee;
        border-radius: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
      }
      &-subtitle {
        margin-left: 8px;
      }
    }
  }
  &__socials {
    border-top: 1px solid #e2e6ee;
  }
}

.aside__main {
  padding-right: 20px;
}
.aside__block {
  display: flex;
  flex-direction: column;
  // gap: 12px;
  border-top: 1px solid #e2e6ee;
  padding-top: 16px;
  padding-bottom: 16px;
}
.gap-10 {
  gap: 10px;
}
.gap-12 {
  gap: 12px;
}
</style>
