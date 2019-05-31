<script>
  import Location from '../static/location.svg';
  import Phone from '../static/phone.svg';
  import Mail from '../static/mail.svg';

  const phone = '+380934786191';
  const mail = 'skolzinn@gmail.com';

  function clipboard(field) {
    navigator.clipboard.writeText(field);
  }
</script>

<style>
  section {
    max-width: 800px;
    margin: 20px;
    padding: 20px;
    background: #2c2e2d;
    box-shadow: 0 14px 28px rgba(0,0,0,0.25), 0 10px 10px rgba(0,0,0,0.22);
  }
  .concats {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-between;
  }
  .contact,
  .contact-copy {
    display: flex;
    justify-content: flex-start;
    align-items: center;
    margin-bottom: 25px;
    margin-right: 25px;
  }

  .contact-copy:hover {
    color: #C7F954;
    text-shadow: 0 0 2px #393a33, 0 0 35px #ffffff44, 0 0 8px #f39f0575, 0 0 2px #f39f0575;
  }

  img {
    height: 18px;
    width: 18px;
  }

  span {
    margin-left: 15px;
  }
</style>

<section>
  <div class='concats'>
    <div class='contact'>
      <img src={Location} alt='styled-components'/>
      <span>Kiev</span>
    </div>
    <div
      class='contact-copy'
      style="cursor: pointer;"
      title="Don't call me. I sleep"
      on:click={() => clipboard(phone)}>
      <img src={Phone} alt="Don't call me"/>
      <span>{phone}</span>
    </div>
    <div class='contact-copy' style="cursor: pointer;" on:click={() => clipboard(mail)}>
      <img src={Mail} alt='styled-components'/>
      <span>{mail}</span>
    </div>
  </div>
  <p>Love sneakers, tech wear. 
  Hate aggression. 
  Love my cat Mao.</p>
</section>