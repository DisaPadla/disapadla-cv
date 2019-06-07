<script>
  import Git from '../static/git.svg';
  import Javascript from '../static/javascript.svg';
  import React from '../static/React.svg';
  import Redux from '../static/redux.svg';
  import Styled from '../static/styled.svg';
  import Jest from '../static/jest.svg';
  import Webpack from '../static/webpack.svg';
  import Less from '../static/Less.svg';
  import Mocha from '../static/mocha.svg';
  import Chai from '../static/chai.svg';
  import RxJs from '../static/rxjs.svg';

  const stack = {
    Javascript,
    Git,
    React,
    Redux,
    Styled,
    Jest,
    Webpack,
    Less,
    Mocha,
    Chai,
    RxJs,
  };

  export let title;
  export let time;
  export let p;
  export let technologies;
</script>

<style>
  @keyframes entrance-card {
    0% {
      transform: translateY(-1000px);
      opacity: 0;
    }
    100% {
              transform: translateY(0);
      opacity: 1;
    }
  }

  @keyframes entrance-time {
    0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
  }

	section {
    position: relative;
    display: flex;
    flex-direction: column;
    max-width: 800px;
    padding-bottom: 30px;
    padding-left: 50px;
    background: #2c2e2d;
    animation: entrance-card 1s cubic-bezier(0.250, 0.460, 0.450, 0.940) both;
    animation-iteration-count: 1;
    border-bottom: 1px dashed #D6DFE0;
  }

  .time-section {
    position: absolute;
    left: -32px;
    top: -11px;
    width: 22px;
    height: 22px;
    margin-left: 20px;
    border: 3px solid #D6DFE0;
    border-radius: 50%;
    background: #252827;
  }
  .time-section__time {
    position: absolute;
    left: -180px;
    text-align: end;
    font-size: 14px;
    color: #d5dfe0;
    width: 160px;
    animation: entrance-time 2s cubic-bezier(0.550, 0.085, 0.680, 0.530) both;
  }

  .content {
    padding: 10px;
    font-size: 16px;
    line-height: 2rem;
  }

  .header {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
  }

  img {
    width: 25px;
    height: 25px;
    margin-right: 10px;
  }
</style>

<section>
  <div class='time-section'>
    <span class='time-section__time'>{time}</span>
  </div>
  <div class='content'>
    <div class='header'>
      <h3>{title}</h3>
       <div>
        {#each technologies as tech}
          <img src={stack[tech]} alt={tech} title={tech}/>
        {/each}
      </div>
    </div>
    {@html p}
  </div>
</section>