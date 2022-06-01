<template>
  <div>
    <!--FOOTER-->
    <footer class="footer">
      <p>Quote generator, Copyright &copy; 2022 develop by Joan Kouloumba</p>
      <div>
        <ul class="social-media">
          <li>
            <a
              href="https://www.linkedin.com/in/joan-kouloumba-570a7680/"
              target="_blank"
              ><i class="fa-brands fa-linkedin-in"></i
            ></a>
          </li>
          <li>
            <a href="https://twitter.com/joanKouloumba" target="_blank"
              ><i class="fa-brands fa-twitter"></i
            ></a>
          </li>
          <li>
            <a href="https://github.com/jokoul" target="_blank"
              ><i class="fa-brands fa-github"></i
            ></a>
          </li>
        </ul>
        <p>
          <a
            href="https://joan-kouloumba.in/professional-site/index.html#achievements"
            >Visit more site like this on the professional site.</a
          >
        </p>
      </div>
    </footer>
  </div>
</template>

<style lang="scss" scoped>
/*FOOTER*/
.footer {
  height: auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: linear-gradient(var(--green), var(--green));
  background: -webkit-linear-gradient(#62aacf, #62aacf);
  background: -moz-linear-gradient(#62aacf, #62aacf);
  background: -o-linear-gradient(#62aacf, #62aacf);
  border-radius: 10px;
  padding: 1rem;
  margin-top: 3rem;
  position: relative;
  bottom: 0;
  width: 100%;
  & p {
    font-size: 1.2rem;
    color: white;
    text-align: center;
  }
  & div {
    margin-left: 2rem;
  }
  & p a {
    text-decoration: none;
    color: var(--tertiary);
  }
  & p a:hover {
    text-decoration: underline;
    cursor: pointer;
  }
  & ul {
    display: flex;
    justify-content: space-around;
    align-items: center;
    color: #5d12e7 !important;
    margin-bottom: 1rem;
  }
  & ul li a {
    color: white;
  }
  & ul li {
    transition: all 0.2s;
    list-style-type: none;
  }
  .footer ul li:hover {
    transform: scale(1.3);
  }
  @media screen and (max-width: 450px) {
    .footer {
      flex-direction: column-reverse;
    }
    footer div {
      margin-left: 0;
      margin-bottom: 0;
    }
  }
}
</style>
