<template>
  <div>
    <h3 class="text-xl font-semibold"><strong>Who am I?</strong></h3>
    <p>
      My name is <strong>Bob Bass</strong>, I own
      <a href="narro.app" target="_blank">Narro Automation</a>. I do small
      business automation. Currently, my startup
      <a href="debtcollect.io" target="_blank">DebtCollect.io</a> is placing in
      the top 10 globally with the
      <a href="pioneer.app" target="_blank">Pioneer</a> startup competition.
      DebtCollect will launch this month (October of 2020) for beta users.
    </p>
    <br />
    <h3 class="text-xl font-semibold"><strong>Programming</strong></h3>
    <p>
      I got my start with C#/.NET, the flagship Microsoft programming language
      and framework, but I fell in love with NodeJS as I 'matured' a bit 😉. My
      preferred stack is:
    </p>
    <br />
    <ul class="repeating-counter-rule">
      <b class="text-lg">Current</b>
      <li
        :class="language.logo"
        v-for="language in this.programmingLanguages"
        :key="language"
      >
        {{ language.name }}
      </li>
      <br />
      <b class="text-lg">Learning</b>
      <li :class="learn.logo" v-for="learn in this.learning" :key="learn">
        {{ learn.name }}
      </li>
    </ul>
    <br /><br />
    <hr />
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: "About Me",
      programmingLanguages: [
        { name: "MySQL - Database", logo: "mysql" },
        { name: "Express - Node Framework", logo: "express" },
        { name: "Vue - Front-end JavaScript Framework", logo: "vue" },
        {
          name: "Vuetify - Material Design Component Library",
          logo: "vuetify",
        },
        { name: "Node - Runtime", logo: "node" },
      ],
      learning: [
        { name: "Nuxt", logo: "nuxt" },
        { name: "Tailwinds", logo: "tailwinds" },
      ],
    };
  },
  head() {
    return {
      title: this.title,
      meta: [
        {
          hid:
            "Informaton about Bob Bass, the owner of Narro Automation. See the software stack and resources listed",
          name: "Narro, LLC | About - Bob",
          content: "About Bob, the owner of Narro, LLC",
        },
      ],
    };
  },
};
</script>

<style scoped>
* {
  padding: 0 5%;
}
a {
  color: green;
  font-weight: 500;
  padding: 0;
}
b,
strong {
  padding: 0;
}
ul {
  padding-left: 10%;
  font-weight: 500;
}
li.mysql::before {
  content: "▤ ";
}
li.express::before {
  content: "Ξ ";
}
li.vue::before {
  content: "⩔ ";
}
li.vuetify::before {
  content: "⩒ ";
}
li.nuxt::before {
  content: "⨇ ";
}
li.node::before {
  content: "⬢ ";
}
li.tailwinds::before {
  content: "₸ ";
}
</style>