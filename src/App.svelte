<script>
import page from 'page'; 
  import viteLogo from '/vite.svg'
  import svelteLogo from './assets/svelte.svg'



import Home from'./pages/Home.svelte';  
import About from './pages/About.svelte';
import Profile from './pages/Profile.svelte';

     let current = Home;    
     
    page('/', () => (current = Home)); 
    page('/about', () => (current = About));  
    page('/profile', () => (current = Profile));    

    page.start();
</script>


<main class="flex flex-col pt-[30vh]  bg-[#111] h-[100vh] w-full text-white/90">
  <nav class="mb-6">    
          <a href="/">home</a>    
          <a href="/about">about</a>    
          <a href="/profile">profile</a>  
          </nav>  
          
          <svelte:component this={current} />
          
  <div class="flex flex-row justify-center align-center w-full mx-auto ">
    <a href="https://vitejs.dev" target="_blank"> 
      <img  src={viteLogo} class="logo" alt="Vite Logo" />
    </a>
    <a href="https://svelte.dev" target="_blank"> 
      <img src={svelteLogo} class="logo svelte" alt="Svelte Logo" />
    </a>
  </div>


  <h1 class="text-5xl text-center font-black">

  <span class="bg-gradient-to-r from-cyan-500 to-purple-700 bg-clip-text text-transparent">
  Vite</span>
   + 
     <span class="bg-gradient-to-r from-orange-600 to-orange-500 bg-clip-text text-transparent">
     Svelte
    </span>
   </h1>

  <div class="card mt-6">
  
  </div>

  <p class="text-center mb-2">
    Check out <a href="https://github.com/sveltejs/kit#readme" target="_blank">SvelteKit</a>, the official Svelte app framework powered by Vite!
  </p>

  <p class="text-center">
    Click on the Vite and Svelte logos to learn more
  </p>
</main>

<style>
  .logo {
    height: 6em;
    padding: 1.5em;
    will-change: filter;
  }
  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }
  .logo.svelte:hover {
    filter: drop-shadow(0 0 2em #ff3e00aa);
  }
  main {    
      text-align: center;    
      padding: 1em;    
      max-width: 240px;    
      margin: 0 auto;  
      }  
      h1 {    
        color: #ff3e00;    
        text-transform: uppercase;    
        font-size: 4.5em;    
        font-weight: 900;  
        }  
        @media (min-width: 640px) {    
          main {      
            max-width: none;    
            }  
          }  
    nav a {    
      padding-right: 3rem;  
      }
</style>
