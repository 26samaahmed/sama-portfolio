<svelte:head>
  <title>Sama's Coding Portfolio</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Goldman:wght@400;700&display=swap" rel="stylesheet">
</svelte:head>

<script>
  import NavBar from '../../components/NavBar.svelte';
  import college_highlight1 from '$lib/assets/college_highlight1.jpg';
  import college_highlight3 from '$lib/assets/college_highlight3.jpg';
  import college_highlight5 from '$lib/assets/college_highlight5.jpg';
  import college_highlight7 from '$lib/assets/college_highlight7.jpg';
  import college_highlight9 from '$lib/assets/college_highlight9.jpg';
  import resume from '$lib/assets/Sama_Ahmed_2024_Resume.pdf';
  

  let projects =[
    {name: 'SkySong', link: 'https://github.com/26samaahmed/skysong', teck_stack: 'spotify api, openweather api, python, flask, html, css, spotipy', description: 'A website where the current temperature is displayed and songs of the hour are recommended for people to listen to. The lower the temperature, the calmer the music. If the temperature is high, then upbeat music will be recommended.'},
    {name: 'Concert Tracker', link: 'https://github.com/26samaahmed/concert-tracker', teck_stack: 'ticketmaster api, sveltekit, html, css, javascript', description: 'A website where users can search for concerts by city name and month and see the upcoming concerts in that city.'},
    {name: 'Fullybeyond', link: 'https://github.com/26samaahmed/fullybeyond', teck_stack: 'sveltekit, tailwindCSS, javascript', description: 'A website for CSUF\'s first student-led designathon that shows information about the event like the schedule, sponsors, and judges developed with 4 other team members.'},
    {name: 'acmcsuf.com', link: 'https://github.com/26samaahmed/acmcsuf.com', teck_stack: 'sveltekit, typescript', description: 'A website for the Association for Computing Machinery at California State University, Fullerton with 50+ contributers that shows information about the club, events, and resources. As the webmaster, I am responsible for maintaining the website and updating it with new information.'},
  ]

  let college_highlights = [
    {img: college_highlight1, title: 'Open Source Software Team Member', info: '📍End of Semester Ceremony, Fall 2023'},
    {img: college_highlight5, title: 'ACM CSUF Design Officer', info: '📍End of Semester Meeting, Spring 2024'},
    {img: college_highlight3, title: 'FullyHacks Design Officer', info: '📍Hackathon with 400+ applicants, Spring 2024'},
    {img: college_highlight9, title: 'Open Source Software Co-Team Lead/Webmaster', info: '📍First Contributions Workshop, Fall 2024'},
  ]

</script>

<main>
  <NavBar />
  <div class="flex flex-col border-black border-4 ml-5 mr-5 sm:ml-10 sm:mr-10 mt-10 text-center rounded-md p-16 pl-10 pr-10 sm:p-24 md:p-24 lg:p-24 lg:pt-28 lg:pb-28 xl:p-52" id="intro-container">
    <h1 class="text-3xl sm:text-4xl md:text-6xl xl:text-7xl mb-10"> Sama Ahmed</h1>
    <h2 class="text-lg sm:text-xl md:text-3xl xl:text-4xl mb-5">computer science student <br> @california state university, fullerton</h2>
    <h2 class="text-lg sm:text-xl md:text-2xl xl:text-3xl mb-6">check out my resume <a href={resume} target="_blank" class="text-blue-500">here</a></h2>
  </div>

  <div class="flex flex-col ml-5 mr-5 sm:ml-10 sm:mr-10 mt-24">
    <h1 class="text-3xl sm:text-4xl mb-5">College Highlights</h1>
    <div class="flex flex-wrap">
      {#each college_highlights as highlight}
        <div class="w-full sm:w-1/2 p-2 mb-12 text-center">
          <img src={highlight.img} alt={highlight.title} class="rounded-md mb-5 h-64 lg:h-96 w-full object-cover"/>
          <p>{highlight.title}</p>
          <p>{highlight.info}</p>
        </div>
      {/each}
    </div>
  </div>
  

  <div class="flex flex-col ml-5 mr-5 sm:ml-10 sm:mr-10 mt-24" id="projects">
    <h1 class="text-4xl text-black mb-5">Projects</h1>
    {#each projects as project}
      <div class="flex flex-col bg-black text-white rounded-xl p-5 mb-7" id="project-container">
        <h2 class="text-2xl mb-2">{project.name}</h2>
        <h3 class= "mb-2">Tech Stack: {project.teck_stack}</h3>
        <p class= "mb-2">- {project.description}</p>
        <a href={project.link} target="_blank" class="text-blue-500">View Project</a>
      </div>
    {/each}
    <p class="text-lg text-black mb-5 text-end mr-4">Check out more on my <a class="underline " href="https://github.com/26samaahmed" target="_blank">github</a></p>
  </div>
  <div class="text-center mt-10 m-5">
    <p class="text-md mb-2">Thank you for making it this far! Here is a song recommendation for you:</p>
    <iframe 
      style="border-radius:12px; display:block; margin:auto;" 
      class="w-full sm:w-96"
      src="https://open.spotify.com/embed/track/52dF752HWIsv2CpSuTX3p2?utm_source=generator" 
      height="100"
      frameBorder="0" 
      allowfullscreen 
      allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" 
      loading="lazy" 
      title="Spotify Song Player">
    </iframe>
  </div>
  <p class="text-center mt-5 text-md md:text-lg text-black">Made with 💚 by Sama Ahmed</p>
</main>

<style>
  :global(body) {
    background-color: white;
    font-family: "Goldman", sans-serif;
  }

  #intro-container {
    transition: 0.3s;
  }
  #intro-container:hover {
    background-color: black;
    color: white;
  }

  #project-container {
    transition: 0.3s;
  }

  #project-container:hover {
    background-color: white;
    color: black;
    border: 2px solid black;
  }
</style>