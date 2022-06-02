<template>
  <footer id="footer">
    <div>
      <h4>email</h4>
      <a href="mailto:rmsgur2275@gmail.com">rmsgur2275@gmail.com</a>
    </div>
    <div>
      <h4>KaKao</h4>
      <a href="#">q_4113</a>
    </div>
    <div>
      <h4>social</h4>
      <ul>
        <li><a href="/">Youtube</a></li>
        <li><a href="/">Instargram</a></li>
        <li><a href="/">Github</a></li>
        <li><a href="/">Referecne</a></li>
        <li><a href="/">Tutorials</a></li>
      </ul>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
#footer {
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100%;
  color: var(--white);
  border-top: 1px solid var(--dark_border);
  background-color: var(--dark_bg);
  display: flex;
  align-items: center;
  font-family: "Rajdhani";
  z-index: 99999;

  div {
    text-align: center;
    padding: 1.45rem;
  }
  h4,
  ul {
    display: inline-block;
  }

  a {
    position: relative;

    &::before {
      content: "";
      position: absolute;
      left: 0;
      bottom: 0;
      width: 100%;
      height: 1px;
      background: var(--white);
      transform: scaleX(0);
      transition: all 0.3s ease;
    }
    &:hover::before {
      transform: scaleX(1);
    }
  }

  h4 {
    font-weight: 600;
    padding: 0 0.6em;
    text-transform: capitalize; //앞글자만 대문자
  }

  div:nth-child(1) {
    flex: 1 1 25%;
    border-right: 1px solid var(--dark_border);
  }
  div:nth-child(2) {
    flex: 1 1 20%;
    border-right: 1px solid var(--dark_border);
  }
  div:nth-child(3) {
    flex: 1 1 55%;

    li {
      display: inline;

      a {
        display: inline-block;
        padding: 0 0.6em;
        position: relative;

        &::before {
          content: "";
          position: absolute;
          left: 0.6rem;
          bottom: 0;
          width: calc(100% - 1.2em);
          height: 1px;
          background: var(--white);
          transform: scaleX(0);
          transition: all 0.3s ease;
        }
        &:hover::before {
          transform: scaleX(1);
        }
      }
    }
  }
}
// 라이트 버전
.light#footer {
  background-color: var(--light_bg);
  border-color: var(--light_border);

  h4 {
    color: var(--black);
  }
  a {
    color: var(--black);

    &::before {
      background: var(--black);
    }
  }
  div {
    border-right-color: var(--light_border);

    li {
      a {
        &::before {
          background: var(--black);
        }
      }
    }
  }
}
</style>
