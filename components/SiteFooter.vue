<template>
  <div class="footer-bg">
    <div class="container flex">
      <div class="footerLeft">
        <p>2020 SSU ORGANISATION</p>
        <a>
          <img id="logo" src="img/logo.svg" />
        </a>
      </div>
      <div>
        <ul class="footerRight">
         <li>
          <a href="team">Team</a>
        </li>
        <li>
          <a href="content">Content</a>
        </li>
        <li>
          <a href="staff">Staff</a>
        </li>
        <li>
          <a href="sponsors">Sponsors</a>
        </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>


.footerLeft {
  color: white;
}

.footerRight {
  display: flex;
  list-style: none;
  flex-direction: row;
  justify-content: space-between;
}

.footer-bg {
  padding: 50px 0;
  background-color: #011321;
  display: flex;
  border-top: inset 1px white;
}

.container {
  flex-direction: row;
  justify-content: space-between;
  text-align: left;
}

ul {
  display: flex;
  flex-direction: column;
  list-style: none;
  padding: 0;
}

ul li {
  color: #ffffff;
}

#logo {
  width: 40px;
  margin-top: 50px;
}

ul li a {
        padding: 26px;
        color: white;
        text-decoration: none;
    }

    ul li a:hover {
        background-color: white;
    color: #011321;
    box-shadow: inset 0px 4px #ce922a;
    cursor: pointer;
    }

@media only screen and (max-width: 420px) {
    .footerRight {
        display: none;
    }

    #logo {
        text-align: center;
    }

    .footer-bg {
        align-items: center;
    }

    ul {
        flex-direction: row;
        
    }

    .container {
        text-align: center;
        margin: auto;
    }
}
</style>