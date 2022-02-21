<template>
  <div class="landing-container">
    <div class="hero">
      <div class="container">
        <div class="header">
          <a href="">
            <img src="@/assets/logo.svg" alt="">
          </a>
          <a class="header-btn" target="_blank" href="https://partisiablockchain.com/">Visit Foundation</a>
        </div>
        <h1>
          Developing Applications to help grow the Partisia Blockchain Ecosystem
        </h1>
        <p>Building, operating and promoting applications within the Partisia Blockchain ecosystem.</p>
        <button>Contact Us</button>
      </div>
    </div>
    <div class="philosophy">
      <div class="philosophy-inner">
        <div class="container">
          <h2>Our <span>Core</span> Philosophies</h2>
          <div class="cores row">
            <div class="col-md-4 col-12">
              <div class="core-card">
                <div class="core-img">
                  <img src="@/assets/core-1.svg" alt="">
                </div>
                <h4>Global Minded</h4>
                <p>Amet minim mollit non deserunt ullamco est sit aliqua dolor . consequat duis enim velit</p>
              </div>
            </div>
            <div class="col-md-4 col-12">
              <div class="core-card">
                <div class="core-img">
                  <img src="@/assets/core-2.svg" alt="">
                </div>
                <h4>Rapid Development</h4>
                <p>Amet minim mollit non deserunt ullamco est sit aliqua dolor . consequat duis enim velit</p>
              </div>
            </div>
            <div class="col-md-4 col-12">
              <div class="core-card">
                <div class="core-img">
                  <img src="@/assets/core-3.svg" alt="">
                </div>
                <h4>Sustainable</h4>
                <p>Amet minim mollit non deserunt ullamco est sit aliqua dolor . consequat duis enim velit</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="projects">
      <div class="container">
        <h2>Our <span>Awesome</span> Projects</h2>
        <div class="project" v-for="(project, index) of projects" :key="index">
          <div class="left">
            <div class="partisia">
              <img src="@/assets/partisia.svg" alt="">
            </div>
            <div class="detail">
              <h4>{{ project.title }}</h4>
              <p>{{ project.description }}</p>
            </div>
          </div>
          <div class="right">
            <div class="wallet">{{ project.action }}</div>
            <a :href="project.link" target="_blank" class="get-link">Get</a>
          </div>
        </div>
      </div>
    </div>
    <div class="work-with-us">
      <div class="work-with-us-inner">
        <div class="container">
          <h2>Work With Us!</h2>
          <p>With deep technical expertise in blockchain and distributed computing, we are available for one-on-one consulting projects.</p>
          <button>Contact Us</button>
        </div>
      </div>
    </div>
    <div class="footer">
      <div class="container">
        <div class="top-footer">
          <div class="left">
            <img src="@/assets/footer-logo.svg" alt="">
            <p>Building, operating and promoting applications within the Partisia Blockchain ecosystem.</p>
          </div>
          <div class="right">
            <ul>
              <h5>Our Products</h5>
              <li><a href="https://chrome.google.com/webstore/detail/partisia-wallet/gjkdbeaiifkpoencioahhcilildpjhgh" target="_blank">Partisia Wallet Chrome</a></li>
              <li><a href="https://addons.mozilla.org/en-US/firefox/addon/partisia-wallet/" target="_blank">Partisia Wallet Firefox</a></li>
              <li><a href="https://mpcexplorer.com/" target="_blank">MPC Explorer</a></li>
            </ul>
            <ul>
              <h5>About Us</h5>
              <li><a href="https://jobs.ashbyhq.com/partisiablockchain" target="_blank">We’re Hiring</a></li>
              <li><a href="">Contact Us</a></li>
              <li><a href="https://partisiablockchain.com/" target="_blank">Partisia Blockchain</a></li>
            </ul>
          </div>
        </div>
        <div class="bottom-footer">
          <span>
            PBC Apps All Rights Reserved © 2022
          </span>
          <div class="links">
            <a href="">Terms of Use</a>
            <div></div>
            <a href="">About Us</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Landing',
  data() {
    return {
      projects: [
        {
          title: 'Partisia Chrome Wallet',
          description: 'A Partisia Wallet Extension for your browser. This is an extension for accessing the Partisia Blockchain MPC token and Dapps that run on Partisia Blockchain.',
          action: 'Wallet',
          link: 'https://chrome.google.com/webstore/detail/partisia-wallet/gjkdbeaiifkpoencioahhcilildpjhgh'
        },
        {
          title: 'Partisia Firefox Wallet',
          description: 'A Partisia Wallet Extension for your browser. This is an extension for accessing the Partisia Blockchain MPC token and Dapps that run on Partisia Blockchain.',
          action: 'Wallet',
          link: 'https://addons.mozilla.org/en-US/firefox/addon/partisia-wallet/'
        },
        {
          title: 'MPC Explorer',
          description: 'MPC Block Explorer is a comprehensive network explorer highlighting core Partisia Blockchain statistics. View Validator information, cluster data, transaction throughput, and more.',
          action: 'Explorer',
          link: 'https://mpcexplorer.com/'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.landing-container {
  button, .header-btn, .get-link {
    font-family: 'Ubuntu';
    font-style: normal;
    font-weight: bold;
    font-size: 1rem;
    line-height: 110%;
    padding: 1rem 3.5rem;
    background: #00EE98;
    border-radius: 4px 4px 12px 4px;
    border: none;
    outline: none;
    color: white;
    text-decoration: none !important;
    &.header-btn {
      padding: 0.75rem 3rem;
    }
    &:hover {
      background: darken($color: #00EE98, $amount: 0.9);
    }
  }
  .container {
    @media (max-width: 992px) {
      padding-left: 1.5rem;
      padding-right: 1.5rem;
    }
  }
  .hero {
    padding-bottom: 7.5rem;
    background: url('~@/assets/hero-bg.png');
    background-repeat: no-repeat;
    background-size: cover;
    @media (max-width: 992px) {
      background: url('~@/assets/hero-bg-mobile.png');
      background-repeat: no-repeat;
      background-size: cover;
      padding-bottom: 20.5rem;
    }
    .header {
      height: 6.25rem;
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 3.75rem;
      @media (max-width: 992px) {
        margin-bottom: 4rem;
      }
    }
    h1 {
      font-style: normal;
      font-weight: bold;
      font-size: 3.375rem;
      line-height: 120%;
      letter-spacing: 0.02em;
      color: #FFFFFF;
      margin-bottom: 1rem;
      max-width: 42.75rem;
      @media (max-width: 992px) {
        font-style: normal;
        font-weight: bold;
        font-size: 1.625rem;
        line-height: 120%;
        letter-spacing: 0.02em;
        color: #ffffff;
        max-width: none;
      }
    }
    p {
      font-family: Montserrat;
      font-style: normal;
      font-weight: normal;
      font-size: 1.125rem;
      line-height: 150%;
      letter-spacing: 0.02em;
      color: rgba($color: #ffffff, $alpha: 0.8);
      margin-bottom: 2.5rem;
      max-width: 42.75rem;
      @media (max-width: 992px) {
        font-size: 1rem;
        margin-bottom: 4rem;
        max-width: none;
      }
    }
  }
  .philosophy {
    padding: 2rem;
    @media (max-width: 992px) {
      padding: 2rem 1.5rem;
    }
    .philosophy-inner {
      padding-top: 3.375rem;
      padding-bottom: 5.75rem;
      background: url('~@/assets/core-bg.png');
      background-repeat: no-repeat;
      background-size: cover;
      border-radius: 1rem;
      @media (max-width: 992px) {
        background: url('~@/assets/core-bg-mobile.png');
        background-repeat: no-repeat;
        background-size: cover;
        padding-top: 2rem;
        padding-bottom: 0.5rem;
      }
      h2 {
        font-family: Montserrat;
        font-style: normal;
        font-weight: bold;
        font-size: 2rem;
        line-height: 150%;
        letter-spacing: 0.05em;
        color: #020136;
        margin-bottom: 5.5rem;
        @media (max-width: 992px) {
          font-size: 1.125rem;
          margin-bottom: 2.5rem;
        }
        span {
          color: #00CF91;
          margin-left: 0.25rem;
          margin-right: 0.25rem;
        }
      }
      .cores {
        .core-card {
          background: #FFFFFF;
          box-shadow: 0px 4px 40px rgba(0, 0, 0, 0.04);
          border-radius: 1rem;
          padding: 1.5rem;
          @media (max-width: 992px) {
            margin-bottom: 1.5rem;
          }
          .core-img {
            width: 90px;
            height: 90px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg, #110CE4 0%, #0C09AE 100%);
            border-radius: 0.375rem;
            margin-bottom: 1.5rem;
            @media (max-width: 992px) {
              margin-bottom: 1rem;
            }
          }
          h4 {
            font-family: Montserrat;
            font-style: normal;
            font-weight: bold;
            font-size: 1.5rem;
            line-height: 1.875rem;
            color: #020136;
            margin-bottom: 1rem;
            @media (max-width: 992px) {
              font-size: 1rem;
              line-height: 1.25rem;
              margin-bottom: 0.5rem;
            }
          }
          p {
            font-family: Montserrat;
            font-style: normal;
            font-weight: normal;
            font-size: 1.125rem;
            line-height: 150%;
            margin-bottom: 0;
            color: rgba($color: #020136, $alpha: 0.56);
            @media (max-width: 992px) {
              font-size: 0.875rem;
            }
          }
        }
      }
    }
  }
  .projects {
    margin-bottom: 3rem;
    @media (max-width: 992px) {
      margin-top: 1.25rem;
    }
    h2 {
      font-family: Montserrat;
      font-style: normal;
      font-weight: bold;
      font-size: 2rem;
      line-height: 150%;
      letter-spacing: 0.05em;
      color: #020136;
      margin-bottom: 2rem;
      span {
        color: #00CF91;
        margin-left: 0.25rem;
        margin-right: 0.25rem;
      }
      @media (max-width: 992px) {
        font-size: 1.125rem;
        margin-bottom: 1.5rem;
      }
    }
    .project {
      padding-bottom: 1.5rem;
      border-bottom: 1px solid #DFDEE8;
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 2rem;
      @media (max-width: 992px) {
        flex-direction: column;
      }
      .left {
        display: flex;
        align-items: center;
        @media (max-width: 992px) {
          flex-direction: column;
          align-items: flex-start;
        }
        .partisia {
          margin-right: 1.5rem;
          background: #0E0AB4;
          border-radius: 0.5rem;
          width: 6.25rem;
          height: 6.25rem;
          display: flex;
          align-items: center;
          justify-content: center;
          @media (max-width: 992px) {
            margin-bottom: 1rem;
          }
        }
        .detail {
          display: flex;
          flex-direction: column;
          justify-content: center;
          h4 {
            font-family: Montserrat;
            font-style: normal;
            font-weight: bold;
            font-size: 1.125rem;
            line-height: 1.375rem;
            letter-spacing: 0.01em;
            color: #020136;
            margin-bottom: 0.5rem;
          }
          p {
            font-family: Montserrat;
            font-style: normal;
            font-weight: normal;
            font-size: 1.125rem;
            line-height: 150%;
            color: rgba(2, 1, 54, 0.56);
            margin-bottom: 0;
            max-width: 50rem;
            @media (max-width: 992px) {
              max-width: none;
            }
          }
        }
      }
      .right {
        display: flex;
        flex-direction: column;
        align-items: flex-end;
        width: 100%;
        @media (max-width: 992px) {
          flex-direction: row-reverse;
          justify-content: space-between;
          align-items: flex-end;
          margin-top: 1.5rem;
        }
        .wallet {
          padding: 0.375rem 0.75rem;
          border: 1px solid #CECEE6;
          border-radius: 300px;
          margin-bottom: 1rem;
          font-family: Montserrat;
          font-style: normal;
          font-weight: 600;
          font-size: 0.875rem;
          line-height: 1.25rem;
          color: rgba($color: #858B89, $alpha: 0.7);
          @media (max-width: 992px) {
            margin-bottom: 0;
          }
        }
      }
    }
  }
  .work-with-us {
    padding: 2rem;
    @media (max-width: 992px) {
      padding: 0 1.5rem 2rem;
    }
    .work-with-us-inner {
      background: url('~@/assets/work-bg.png');
      background-repeat: no-repeat;
      background-size: cover;
      border-radius: 1rem;
      padding-top: 2.75rem;
      @media (max-width: 992px) {
        background: url('~@/assets/work-bg-mobile.png');
        background-repeat: no-repeat;
        background-size: cover;
        padding-top: 0;
        border-radius: 1rem;
      }
      .container {
        padding-top: 5.75rem;
        padding-bottom: 8.5rem;
        background-image: url('~@/assets/work-img.png');
        background-repeat: no-repeat;
        background-position: right;
        @media (max-width: 992px) {
          padding-top: 3.25rem;
          padding-bottom: 20rem;
          background-image: url('~@/assets/work-img-mobile.png');
          background-repeat: no-repeat;
          background-position: center bottom;
        }
        h2 {
          font-family: Montserrat;
          font-style: normal;
          font-weight: bold;
          font-size: 2rem;
          line-height: 150%;
          letter-spacing: 0.05em;
          color: #020136;
          margin-bottom: 1rem;
          @media (max-width: 992px) {
            font-size: 1.125rem;
            margin-bottom: 0.5rem;
          }
        }
        p {
          font-family: Montserrat;
          font-style: normal;
          font-weight: 500;
          font-size: 1.125rem;
          line-height: 150%;
          color: #020136;
          margin-bottom: 2rem;
          max-width: 26rem;
          @media (max-width: 992px) {
            font-size: 1rem;
            max-width: none;
            margin-bottom: 1rem;
          }
        }
      }
    }
  }
  .footer {
    background: url('~@/assets/footer-bg.png');
    background-repeat: no-repeat;
    background-size: cover;
    padding-top: 3.375rem;
    padding-bottom: 3rem;
    @media (max-width: 992px) {
      background: url('~@/assets/footer-bg-mobile.png');
      background-repeat: no-repeat;
      background-size: cover;
      padding-top: 3.25rem;
      padding-bottom: 6rem;
    }
    .top-footer {
      display: flex;
      justify-content: space-between;
      border-bottom: 1px solid #35355A;
      padding-bottom: 1.5rem;
      @media (max-width: 992px) {
        padding-bottom: 2.5rem;
        flex-direction: column;
      }
      .left {
        img {
          margin-bottom: 1.5rem;
        }
        p {
          font-family: Montserrat;
          font-style: normal;
          font-weight: normal;
          font-size: 1.125rem;
          line-height: 170%;
          color: rgba($color: #ffffff, $alpha: 0.7);
          margin-bottom: 0;
          max-width: 21.25rem;
          @media (max-width: 992px) {
            max-width: none;
            margin-bottom: 2.5rem;
          }
        }
      }
      .right {
        display: flex;
        @media (max-width: 992px) {
          flex-direction: column;
        }
        ul {
          list-style-type: none;
          padding-left: 0;
          margin-bottom: 0;
          margin-left: 4rem;
          width: 12rem;
          @media (max-width: 992px) {
            margin-left: 0;
            margin-bottom: 2.5rem;
            &:last-child {
              margin-bottom: 0;
            }
          }
          h5 {
            font-family: Montserrat;
            font-style: normal;
            font-weight: 600;
            font-size: 1.25rem;
            line-height: 150%;
            margin-bottom: 1.5rem;
            color: #4B4A6C;
          }
          li {
            margin-bottom: 1rem;
            a {
              font-family: Montserrat;
              font-style: normal;
              font-weight: normal;
              font-size: 16px;
              line-height: 150%;
              color: rgba($color: #ffffff, $alpha: 0.7);
            }
          }
        }
      }
    }
    .bottom-footer {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding-top: 1.5rem;
      padding-bottom: 1.5rem;
      @media (max-width: 992px) {
        flex-direction: column;
        padding-top: 2rem;
        align-items: flex-start;
      }
      span {
        font-family: Montserrat;
        font-style: normal;
        font-weight: normal;
        font-size: 0.875rem;
        line-height: 150%;
        color: rgba($color: #ffffff, $alpha: 0.7);
        @media (max-width: 992px) {
          margin-bottom: 1.5rem;
        }
      }
      .links {
        display: flex;
        align-items: center;
        div {
          width: 0.25rem;
          height: 0.25rem;
          border-radius: 0.25rem;
          background: white;
          margin-left: 1rem;
          margin-right: 1rem;
        }
        a {
          font-family: Montserrat;
          font-style: normal;
          font-weight: normal;
          font-size: 0.875rem;
          line-height: 150%;
          color: rgba($color: #ffffff, $alpha: 0.7);
        }
      }
    }
  }
}
</style>