<script>
  let name = "Maggie"; // Change this to your name
  let favoriteNumber = 4; // Change this to your favorite number
  let bio =
    "Welcome to my site! I'm Maggie, I grew up in a small-ish city called Fairfax, Virginia, a couple miles away from Washington, D.C. and now am a Data Science student at the University of Michigan! I have been a KWK scholar three times over, and have learned so much in my experience! This summer will be my fourth summer as a KWK IA. Keep scrolling to learn a little bit more about me!";
  let hobbies = [
    "👩‍💻 Coding 👩‍💻",
    "📖 Reading 📖",
    "🦉 Studying German 🦉",
    "💃 Dance 💃",
    "🎮 Playing the Sims 4 🎮",
  ]; // List some hobbies

  import ImageCard from "./lib/ImageCard.svelte";
  let cardData = [
    {
      image:
        "https://raw.githubusercontent.com/maggiechristoffersen/svelte-about-me/gh-pages/src/assets/duolingo.jpg",
      title: "Language Learner",
      description:
        "I began studying German my freshman year of high school and really fell in love with it! I advanced my skills enough to skip one of the levels at my high school, and have spent a lot of time on Duolingo honing my knowledge of the language. When I was a freshman in college, I took an intensive course in the language that (proven by a four-hour exam) brought me up to fluency! At school, I'm minoring in the language and hope to use my skills in Germany someday!",
    },
    {
      image:
        "https://raw.githubusercontent.com/maggiechristoffersen/svelte-about-me/gh-pages/src/assets/bookshelf.JPG",
      title: "Avid Reader",
      description:
        "Reading is one of my favorite hobbies! I read nearly every day and try to get through (at least) one book per week. My favorite book of all time is Little Women by Louisa May Alcott. I visited her historic home a couple of years ago and had so much fun! I'm also, of course, a fan of the 2019 movie. I'm currently reading Blue Sisters by Coco Mellors, which is about four sisters and follows similar themes, although it's more modern overall!",
    },
    {
      image:
        "https://raw.githubusercontent.com/maggiechristoffersen/svelte-about-me/gh-pages/src/assets/dance.jpg",
      title: "Dance Hobbyist",
      description:
        "Like many people, I started ballet classes when I was three years old. I stuck with it, though, and dance is still one of my favorite hobbies! I spent my high school years heavily focusing on practicing jazz, ballet, and tap dance, but have expanded a lot since coming to college! I've tried out lyrical, contemporary, and musical theatre classes, as well as swing, jive, and Bollywood! I love trying out these new styles of dance, it makes me feel connected with the world around me in a unique way.",
    },
    {
      image:
        "https://raw.githubusercontent.com/maggiechristoffersen/svelte-about-me/gh-pages/src/assets/kwkwdc.jpg",
      title: "Code Mentor",
      description:
        "I started at Kode With Klossy in 2019 at the Washington, D.C. camp! From there, I did camps in 2020 and 2021 before becoming an IA in 2022. This is my fourth summer as an IA for KWK. I've also worked with Girls in Electrical Engineering and Computer Science (GEECS) at the University of Michigan on an outreach committee to teach young women in the local area about the fundamentals of coding!",
    },
    {
      image:
        "https://raw.githubusercontent.com/maggiechristoffersen/svelte-about-me/gh-pages/src/assets/sims4.png",
      title: "Sims 4 Fanatic",
      description:
        "I love playing the Sims 4! When I was a kid, I spent hours upon hours playing dolls. My imagination is one of my greatest assets! Nowadays, I spend time playing the Sims 4 instead of playing with barbie dolls, which gives me a fun way to unwind after long and stressful work periods at school!",
    },
  ];
</script>

<div class="container">
  <div class="header-img">
    <img
      src="https://raw.githubusercontent.com/maggiechristoffersen/svelte-about-me/gh-pages/src/assets/marge.JPG"
    />
  </div>
  <!-- <h1>About Me</h1> -->
  <h1>Hi, I'm {name}!</h1>
  <!-- <p>My favorite number is <strong>{favoriteNumber}</strong>.</p> -->
  <p>{bio}</p>

  <h2>These are some of my hobbies! ✨</h2>
  <div class="hobbies">
    {#each hobbies as hobby}
      <div class="hobby">{hobby}</div>
    {/each}
  </div>
</div>

<h2>Fun Facts About Me</h2>
<div class="card-container">
  {#each cardData as { image, title, description }}
    <div class="card"><ImageCard {image} {title} {description} /></div>
  {/each}
</div>

<style>
  * {
    font-family: "Outfit", sans-serif;
    font-optical-sizing: auto;
    font-weight: 300;
    font-style: normal;
    color: #201e1f;
  }
  h1 {
    /* color: #2c3e50; */
    font-family: "Outfit", sans-serif;
  }
  .container {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
    text-align: center;
  }
  .hobbies {
    display: flex;
    justify-content: center;
    gap: 15px;
    flex-wrap: wrap;
  }
  .hobby {
    background-color: #beffc7;
    color: #388659;
    padding: 10px 15px;
    border-radius: 5px;
  }
  .card-container {
    display: flex;
    justify-content: center;
    /* flex-direction: column; */
    flex-wrap: wrap;
  }
  .header-img {
    display: flex;
    justify-content: center;
    height: 300px;
    border-radius: 50%;
  }
</style>
