<script>
  import Telegram from '../static/telegram.svg';

  const downloadCV = () => {
    const anchor = document.createElement('a');
    anchor.setAttribute('href','../static/Denis_Skolzin_CV.pdf');
    anchor.setAttribute('download','');
    document.body.appendChild(anchor);
    anchor.click();
    anchor.parentNode.removeChild(anchor);
  }
</script>
<style>
  @keyframes blink {
    10% {
      color: #d5dfe0;
      text-shadow: none;
    }
    10.1% {
      color: #d5dfe0;
      text-shadow: none;
    }
    10.2% {
      color: #d5dfe0;
      text-shadow: none;
    }
    20% {
      color: #d5dfe0;
      text-shadow: none;
    }
    20.6% {
      color: #d5dfe0;
      text-shadow: none;
    }
    30% {
      color: #d5dfe0;
      text-shadow: none;
    }
    45.1% {
      color: #C7F954;
      text-shadow: 0 0 2px #393a33, 0 0 35px #ffffff44, 0 0 8px #f39f0575, 0 0 2px #f39f0575;
    }
    50% {
      color: #C7F954;
      text-shadow: 0 0 2px #393a33, 0 0 35px #ffffff44, 0 0 8px #f39f0575, 0 0 2px #f39f0575;
    }
    55% {
      color: #C7F954;
      text-shadow: 0 0 2px #393a33, 0 0 35px #ffffff44, 0 0 8px #f39f0575, 0 0 2px #f39f0575;
    }
    55.1% {
      text-shadow: none;
    }
    57% {
      text-shadow: none;
    }
    57.1% {
      color: #C7F954;
      text-shadow: 0 0 2px #393a33, 0 0 35px #ffffff44, 0 0 8px #f39f0575, 0 0 2px #f39f0575;
    }
    60% {
      color: #C7F954;
      text-shadow: 0 0 2px #393a33, 0 0 35px #ffffff44, 0 0 8px #f39f0575, 0 0 2px #f39f0575;
    }
    60.1% {
      text-shadow: none;
    }
    65% {
      text-shadow: none;
    }
    65.1% {
      color: #C7F954;
      text-shadow: 0 0 2px #393a33, 0 0 35px #ffffff44, 0 0 8px #f39f0575, 0 0 2px #f39f0575;
    }
    75% {
      color: #C7F954;
      text-shadow: 0 0 2px #393a33, 0 0 35px #ffffff44, 0 0 8px #f39f0575, 0 0 2px #f39f0575;
    }
    75.1% {
      text-shadow: none;
    }
    77% {
      text-shadow: none;
    }
    77.1% {
      color: #C7F954;
      text-shadow: 0 0 2px #393a33, 0 0 35px #ffffff44, 0 0 8px #f39f0575, 0 0 2px #f39f0575;
    }
    85% {
      color: #C7F954;
      text-shadow: 0 0 2px #393a33, 0 0 35px #ffffff44, 0 0 8px #f39f0575, 0 0 2px #f39f0575;
    }
    85.1% {
      text-shadow: none;
    }
    86% {
      text-shadow: none;
    }
    86.1% {
      color: #C7F954;
      text-shadow: 0 0 2px #393a33, 0 0 35px #ffffff44, 0 0 8px #f39f0575, 0 0 2px #f39f0575;
    }
    100% {
      color: #C7F954;
      text-shadow: 0 0 2px #393a33, 0 0 35px #ffffff44, 0 0 8px #f39f0575, 0 0 2px #f39f0575;
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
    animation: blink 1.8s linear 1.1s;
  }

  h2:hover {
    color: #C7F954;
    text-shadow: 0 0 2px #393a33, 0 0 35px #ffffff44, 0 0 8px #f39f0575, 0 0 2px #f39f0575;
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
  <h2 title='I have an alarm which reminds me to stay asleep'>Denis Skolzin</h2>
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