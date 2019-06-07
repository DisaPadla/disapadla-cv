<script>
  import { onMount, afterUpdate } from 'svelte';
  import Telegram from '../static/telegram.svg';
  import { TextScramble } from './scramble-effect';

  const fullName = 'DENIS SKOLZIN';
  const hieroglyphs = '死ぬ愛してる死沈';
  let title = fullName;
  let reverseTitle = false;

  const downloadCV = () => {
    const anchor = document.createElement('a');
    anchor.setAttribute('href', './Denis_Skolzin_CV.pdf');
    anchor.setAttribute('download','');
    document.body.appendChild(anchor);
    anchor.click();
    anchor.parentNode.removeChild(anchor);
  }

  const onClickTitle = () => {
    if (title === fullName) {
      title = hieroglyphs;
    } else {
      title = fullName
    }
  };

  onMount(() => {
		const el = document.querySelector('.title');
    const fx = new TextScramble(el, hieroglyphs);
    fx.setText(title)
  });
  
  afterUpdate(() => {
    const el = document.querySelector('.title');
    const fx = new TextScramble(el, hieroglyphs);
    fx.setText(title)
  });
</script>
<style>
	.header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;

    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    height: 50px;
    padding: 20px;
    background: #252726;
    box-shadow: 0 14px 28px rgba(0,0,0,0.25), 0 10px 10px rgba(0,0,0,0.22);
    z-index: 10;
  }

  h2 {
    position: relative;
    cursor: pointer;
    width: 300px;
  }
  h2:before,
  h2:after {
    display: block;
    content: attr(data-text);
    position: absolute;
    top: 0;
    width: 100%;
    background: #252726;
    clip: rect( 0, 900px, 0, 0 );
    overflow: hidden;
  }
  h2:after {
    animation: glitch-animation 1s infinite linear alternate-reverse;
    left: 2px;
    text-shadow: -1px 0 red;
  }
  h2:before {
    animation: glitch-animation-2 2s infinite linear alternate-reverse;
    left: -2px;
    text-shadow: 1px 0 blue;
  }
  .contacts {
    display: flex;
    justify-content: flex-start;
    width: 200px;
  }

  .cv {
    position: relative;
    font-size: 26px;
    cursor: pointer;
  }

  .cv:before,
  .cv:after {
    display: block;
    content: attr(data-text);
    position: absolute;
    top: 0;
    width: 100%;
    background: #252726;
    clip: rect( 0, 900px, 0, 0 );
    overflow: hidden;
  }
  .cv:after {
    animation: glitch-animation 1s infinite linear alternate-reverse;
    left: 2px;
    text-shadow: -1px 0 red;
  }
  .cv:before {
    animation: glitch-animation-2 2s infinite linear alternate-reverse;
    left: -2px;
    text-shadow: 1px 0 blue;
  }
  .contacts {
    display: flex;
    justify-content: flex-start;
    width: 200px;
  }
  
  .github-corner:hover .octo-arm {
    animation: octocat-wave 560ms ease-in-out;
  }
  @media (max-width: 500px) {
    .octo-arm {
      animation: none;
    }
    .octo-arm {
      animation: octocat-wave 560ms ease-in-out;
    }
  }
</style>

<div class='header'>
  <h2 on:click={onClickTitle} class='title' title='I have an alarm which reminds me to stay asleep' data-text={title}>{title}</h2>
  <div class='contacts'>
    <div class="cv" data-text='CV' on:click={downloadCV}>CV</div>
    <a
      href='https://t.me/DisaPadla'
      target="_blank"
      rel="noreferrer"
      aria-label="View source on GitHub"
      class='github-corner'
    >
      <img src={Telegram} alt='telegram' title='telegram'/>
    </a>
    <a
      href='https://github.com/DisaPadla'
      target="_blank"
      aria-label="View source on GitHub"
      rel="noreferrer"
      class='github-corner'
    >
      <svg
        width="70"
        height="70"
        viewBox="0 0 250 250"
        style="color:#C7F954; position: absolute; top: 5px; border: 0; right: 0; transform: rotate(-45deg);"
        aria-hidden="true"
      >
        <path
          d="M128.3,109.0 C113.8,99.7 119.0,89.6 119.0,89.6 C122.0,82.7 120.5,78.6 120.5,78.6 C119.2,72.0 123.4,76.3 123.4,76.3 C127.3,80.9 125.5,87.3 125.5,87.3 C122.9,97.6 130.6,101.9 134.4,103.2"
          fill="currentColor"
          style="transform-origin: 130px 106px;"
          class="octo-arm"
        ></path>
        <path
          d="M115.0,115.0 C114.9,115.1 118.7,116.5 119.8,115.4 L133.7,101.6 C136.9,99.2 139.9,98.4 142.2,98.6 C133.8,88.0 127.5,74.4 143.8,58.0 C148.5,53.4 154.0,51.2 159.7,51.0 C160.3,49.4 163.2,43.6 171.4,40.1 C171.4,40.1 176.1,42.5 178.8,56.2 C183.1,58.6 187.2,61.8 190.9,65.4 C194.5,69.0 197.7,73.2 200.1,77.6 C213.8,80.2 216.3,84.9 216.3,84.9 C212.7,93.1 206.9,96.0 205.4,96.6 C205.1,102.4 203.0,107.8 198.3,112.5 C181.9,128.9 168.3,122.5 157.7,114.1 C157.9,116.9 156.7,120.9 152.7,124.9 L141.0,136.5 C139.8,137.7 141.6,141.9 141.8,141.8 Z"
          fill="currentColor"
          class="octo-body"
        ></path>
      </svg>
    </a>
  </div>
</div>