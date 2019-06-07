<script>
  import { onMount } from 'svelte';
  import Telegram from '../static/telegram.svg';
  import { TextScramble } from './scramble-effect';

  const fullName = 'DENIS SKOLZIN';

  const downloadCV = () => {
    const anchor = document.createElement('a');
    anchor.setAttribute('href','../static/Denis_Skolzin_CV.pdf');
    anchor.setAttribute('download','');
    document.body.appendChild(anchor);
    anchor.click();
    anchor.parentNode.removeChild(anchor);
  }

  onMount(() => {
		const el = document.querySelector('.title');
    const fx = new TextScramble(el);
    fx.setText(fullName)
	});
</script>
<style>
  @keyframes glitch-animation {
      0% {
        clip: rect(42px, 9999px, 44px, 0);
      }
      1% {
      transform: scaleY(1) skewX(0deg);
      }
      1.5% {
        transform: scaleY(3) skewX(-60deg);
      }
      2% {
        transform: scaleY(1) skewX(0deg);
      }
      5% {
        clip: rect(12px, 9999px, 59px, 0);
      }
      10% {
        clip: rect(48px, 9999px, 29px, 0);
      }
      15.0% {
        clip: rect(42px, 9999px, 73px, 0);
      }
      20% {
        clip: rect(63px, 9999px, 27px, 0);
      }
      25% {
        clip: rect(34px, 9999px, 55px, 0);
      }
      30.0% {
        clip: rect(86px, 9999px, 73px, 0);
      }
      35% {
        clip: rect(20px, 9999px, 20px, 0);
      }
      40% {
        clip: rect(26px, 9999px, 60px, 0);
      }
      45% {
        clip: rect(25px, 9999px, 66px, 0);
      }
      50% {
        clip: rect(57px, 9999px, 98px, 0);
      }
      51% {
      transform: scaleX(1) scaleY(1) skewX(0deg);
      }
        
      52% {
        transform: scaleX(1.5) scaleY(.2) skewX(80deg);
      }
        
      53% {
        transform: scaleX(1) scaleY(1) skewX(0deg);
      }
      55.0% {
        clip: rect(5px, 9999px, 46px, 0);
      }
      60.0% {
        clip: rect(82px, 9999px, 31px, 0);
      }
      65% {
        clip: rect(54px, 9999px, 27px, 0);
      }
      70% {
        clip: rect(28px, 9999px, 99px, 0);
      }
      75% {
        clip: rect(45px, 9999px, 69px, 0);
      }
      80% {
        clip: rect(23px, 9999px, 85px, 0);
      }
      85.0% {
        clip: rect(54px, 9999px, 84px, 0);
      }
      90% {
        clip: rect(45px, 9999px, 47px, 0);
      }
      95% {
        clip: rect(37px, 9999px, 20px, 0);
      }
      100% {
        clip: rect(4px, 9999px, 91px, 0);
      }
    }
    @keyframes glitch-animation-2 {
      0% {
        clip: rect(65px, 9999px, 100px, 0);
      }
      1% {
      transform: scaleY(1) skewX(0deg);
      }
      1.5% {
        transform: scaleY(3) skewX(-60deg);
      }
      2% {
        transform: scaleY(1) skewX(0deg);
      }
      5% {
        clip: rect(52px, 9999px, 74px, 0);
      }
      10% {
        clip: rect(79px, 9999px, 85px, 0);
      }
      15.0% {
        clip: rect(75px, 9999px, 5px, 0);
      }
      20% {
        clip: rect(67px, 9999px, 61px, 0);
      }
      23% {
        transform: scaleX(.95);
      }
      25% {
        clip: rect(14px, 9999px, 79px, 0);
      }
      30.0% {
        clip: rect(1px, 9999px, 66px, 0);
      }
      35% {
        clip: rect(86px, 9999px, 30px, 0);
      }
      40% {
        clip: rect(23px, 9999px, 98px, 0);
      }
      45% {
        clip: rect(85px, 9999px, 72px, 0);
      }
      50% {
        clip: rect(71px, 9999px, 75px, 0);
      }
      51% {
        transform: scaleX(1) scaleY(1) skewX(0deg);
      }
        
      52% {
        transform: scaleX(1.5) scaleY(.2) skewX(80deg);
      }
        
      53% {
        transform: scaleX(1) scaleY(1) skewX(0deg);
      }
      55.0% {
        clip: rect(2px, 9999px, 48px, 0);
      }
      60.0% {
        clip: rect(30px, 9999px, 16px, 0);
      }
      65% {
        clip: rect(59px, 9999px, 50px, 0);
      }
      70% {
        clip: rect(41px, 9999px, 62px, 0);
      }
      75% {
        clip: rect(2px, 9999px, 82px, 0);
      }
      80% {
        clip: rect(47px, 9999px, 73px, 0);
      }
      85.0% {
        clip: rect(3px, 9999px, 27px, 0);
      }
      90% {
        clip: rect(26px, 9999px, 55px, 0);
      }
      95% {
        clip: rect(42px, 9999px, 97px, 0);
      }
      100% {
        clip: rect(38px, 9999px, 49px, 0);
      }
    }

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
  }
  h2:before,
  h2:after {
    display: block;
    content: attr(data-text);
    position: absolute;
  }
  h2:after {
    animation: glitch-animation 1s infinite linear alternate-reverse;
    clip: rect( 0, 900px, 0, 0 );
    left: 2px;
    color: #d5dfe0;
    overflow: hidden;
    background: #252726;
    text-shadow: -1px 0 red;
    width: 100%;
    top: 0;
  }
  h2:before {
    animation: glitch-animation-2 2s infinite linear alternate-reverse;
    color: #d5dfe0;
    clip: rect( 0, 900px, 0, 0 );
    left: -2px;
    background: #252726;
    overflow: hidden;
    text-shadow: 1px 0 blue;
    top: 0;
  }
  .contacts {
    display: flex;
    justify-content: flex-start;
    width: 200px;
  }

  .cv {
    color: #C7F954;
    font-size: 26px;
    cursor: pointer;
  }

  .cv:hover {
    transform: scale(1.1);
  }
  
  .github-corner:hover .octo-arm {
    animation: octocat-wave 560ms ease-in-out;
  }
  @keyframes octocat-wave {
    0%,
    100% {
      transform: rotate(0);
    }
    20%,
    60% {
      transform: rotate(-25deg);
    }
    40%,
    80% {
      transform: rotate(10deg);
    }
  }

  @keyframes giggle {
    0%, 100% {
        transform:translate(-50%,-50%) translateY(-2px);
    }
    50% {
        transform:translate(-50%,-50%) translateY(2px);
    }
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
  <h2 class='title' title='I have an alarm which reminds me to stay asleep' data-text={fullName}>{fullName}</h2>
  <div class='contacts'>
    <div class="cv" on:click={downloadCV}>CV</div>
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