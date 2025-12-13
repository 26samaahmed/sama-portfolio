<script>
  import NavBar from "../../components/NavBar/Technical_NavBar.svelte";
  import Gallery from "../../components/Gallery/Gallery.svelte";
  import Footer from "../../components/Footer/Footer.svelte";

  import highlight_1 from "$lib/assets/highlight_1.jpg";
  import hightlight_2 from "$lib/assets/highlight_2.jpg";
  import hightlight_3 from "$lib/assets/highlight_3.jpg";
  import hightlight_4 from "$lib/assets/highlight_4.jpg";
  import hightlight_5 from "$lib/assets/highlight_5.jpg";
  import hightlight_6 from "$lib/assets/highlight_6.jpg";

  let college_highlights = [
    {
      img: highlight_1,
      title: "College Highlight 1",
    },
    {
      img: hightlight_2,
      title: "College Highlight 2",
    },
    {
      img: hightlight_3,
      title: "College Highlight 3",
    },
    {
      img: hightlight_4,
      title: "College Highlight 4",
    },
    {
      img: hightlight_5,
      title: "College Highlight 5",
    },
    {
      img: hightlight_6,
      title: "College Highlight 6",
    },
  ];

  let projects = [
    {
      name: "SkySong",
      link: "https://github.com/26samaahmed/skysong",
      teck_stack: [
        "Html",
        "CSS",
        "Python",
        "Flask",
        "Openweathermap API",
        "Spotify API",
      ],
      description:
        "☆ A web app that displays the current temperature and recommends songs to match the weather — chill tracks for colder days, upbeat ones for the heat.",
    },
    {
      name: "Concert Tracker",
      link: "https://github.com/26samaahmed/concert-tracker",
      teck_stack: ["SvelteKit", "Ticketmaster API"],
      description:
        "☆ A website where users can search for concerts by city and month, and explore upcoming events happening in that location.",
    },
    {
      name: "FullyBeyond",
      link: "https://github.com/26samaahmed/fullybeyond",
      teck_stack: ["SvelteKit", "Tailwind CSS"],
      description:
        "☆ The official site for csuf’s first student-led designathon, built with a team of 4. It features the event schedule, sponsors, and more.",
    },
    {
      name: "ACM at CSUF website",
      link: "https://github.com/EthanThatOneKid/acmcsuf.com",
      teck_stack: ["SvelteKit", "TypeScript"],
      description:
        "☆ The official website for csuf’s acm chapter, built with 70+ contributors. It highlights club info, events, and resources for members.",
    },
    {
      name: "Playlist Exporter",
      link: "https://github.com/JOwen-ster/PlaylistExporter",
      teck_stack: [
        "Python",
        "Flask",
        "SvelteKit",
        "Tailwind CSS",
        "Spotify API",
        "YouTube API",
      ],
      description:
        "☆ A tool that lets users convert and export their spotify playlists directly to youtube playlists.",
    },
  ];

  let song_url =
    "https://open.spotify.com/embed/track/6Stw2SepJwrkjT60fusHxR?utm_source=generator";

  let color = "#000000";
  let path1 = {
    href: "/",
    text: "Return Home",
  };

  let path2 = {
    href: "/creative-portfolio",
    text: "Explore Creative Portfolio",
  };
</script>

<svelte:head>
  <title>Technical Portfolio - Sama Ahmed</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link
    href="https://fonts.googleapis.com/css2?family=Big+Shoulders+Stencil:opsz,wght@10..72,100..900&display=swap"
    rel="stylesheet"
  />
</svelte:head>

<body class="bg-white text-black">
  <NavBar />
  <div
    class="flex flex-col rounded-md mr-5 ml-5 sm:ml-16 sm:mr-16 sm:pt-28 md:pb-64 text-center"
  >
    <div
      class="flex flex-col sm:flex-row justify-start items-start w-full mb-8 pt-16 text-left"
    >
      <h1
        class="text-2xl sm:text-3xl md:text-5xl xl:text-5xl sm:mr-4 mb-4 sm:mb-0"
      >
        Hi, I'm Sama Ahmed!
      </h1>
    </div>

    <h2 class="text-lg sm:text-xl md:text-3xl xl:text-4xl mb-5 text-left">
      A frontend-focused developer with a passion for building responsive web applications and
      creating seamless user experiences — driven to lead with initiative
      and collaborate with purpose ⋆. 𐙚 ˚
    </h2>
  </div>

  <Gallery {college_highlights} />

  <div class="ml-5 mr-5 sm:ml-16 sm:mr-16 mt-24" id="projects">
    <h1 class="text-4xl text-black mb-2">Projects</h1>
    <div class="flex flex-wrap -mx-2">
      {#each projects as project}
        <div class="w-full sm:w-1/2 lg:w-1/3 pb-8 px-2">
          <div
            class="flex flex-col relative rounded border-black border-2 mt-10 pt-6 px-4 h-full min-h-[10rem] sm:min-h-[10rem]"
          >
            <div
              class="md:flex md:justify-between items-center absolute -top-4 left-4"
            >
              <h2 class="text-2xl bg-white px-3 max-w-full break-words">
                {project.name}
              </h2>
            </div>

            <p class="mb-2 text-lg">{project.description}</p>
            <div class="flex flex-wrap gap-2 mb-2">
              {#each project.teck_stack as stack}
                <p
                  class="bg-black text-sm text-white rounded-lg px-3 py-1 text-center whitespace-nowrap"
                >
                  {stack}
                </p>
              {/each}
            </div>

            <div class="mt-auto mb-2">
              <a
                href={project.link}
                target="_blank"
                class="text-lg text-blue-500 border-b-2 border-transparent hover:border-current transition duration-300 ease-in-out text-center"
                >View Project</a
              >
            </div>
          </div>
        </div>
      {/each}
    </div>

    <p class="text-xl text-black mt-5 text-end mr-4">
      Check out more on my
      <a class="underline" href="https://github.com/26samaahmed" target="_blank"
        >github</a
      >
    </p>
  </div>

  <div class="relative ml-5 mr-5 sm:ml-16 sm:mr-16 mt-40 pt-10 px-4 pb-4">
    <div class="absolute -top-6 left-4 flex items-center">
      <h1 class="bg-white px-3 text-4xl whitespace-nowrap">જ⁀➴ About Me</h1>
    </div>

    <section class="text-xl sm:text-2xl">
      <p>
        I’m an Egyptian immigrant who moved to the United States at 15, bringing
        a unique perspective to my work in tech. I’m passionate about both
        Product Management and Software Engineering, especially frontend
        development. I love building intuitive, user-centered web apps and
        exploring how design, engineering, and product come together to create
        great user experiences.
      </p>
      <br />
      <p>
        Currently, I’m a senior at Cal State Fullerton majoring in Computer
        Science. Since my sophomore year, I’ve been actively involved in ACM at
        CSUF, the largest tech club on campus, taking on leadership roles like
        co-directing Fullyhacks 2025, where I led 50+ organizers and helped
        attract over 250 participants. I also co-led the Open Source team and
        served as Webmaster during the 2024–2025 academic year, teaching
        students about open source tools and helping them contribute to
        projects.
      </p>
      <br />
      <p>
        Outside of tech, I enjoy watching k-dramas, listening to music, and
        designing websites. In 2024, I had the amazing experience of seeing my
        favorite artists, Ateez and TXT, live in concert ⋆ 𐙚 ̊.
      </p>
    </section>
  </div>

  <Footer {song_url} {path1} {path2} {color} />
</body>

<style>
  :global(body) {
    font-family: "Big Shoulders Stencil", sans-serif;
  }
</style>
