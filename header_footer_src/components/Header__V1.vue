<template>
  <header class="pvu__header">
    <!-- first row -->
    <section class="pvu__header-first">
      <div class="pvu__header-menu">
        <div class="pvu__desktop desktop1">
          <div class="pvu__header-links header-links1">
            <div class="pvu__link-text link-text1">
              About
            </div>
            <div class="pvu__link-menu link-menu1">
              <a :href="communityBaseUrl + '/what-is-patentsview'"
                >What Is PatentsView</a
              >
              <a :href="communityBaseUrl + '/glossary'">Glossary</a>
              <a :href="communityBaseUrl + '/about/terms-privacy'"
                >Terms of Use and Privacy</a
              >
            </div>
          </div>
          <div class="pvu__header-links header-links1">
            <div class="pvu__link-text link-text1">
              Methods & Sources
            </div>
            <div class="pvu__link-menu link-menu1">
              <a :href="communityBaseUrl + '/disambiguation'">Disambiguition</a>
              <a :href="communityBaseUrl + '/gender-attribution'"
                >Gender Attributes</a
              >
              <a :href="communityBaseUrl + '/government-interest'"
                >Government Interests</a
              >
            </div>
          </div>
          <div class="pvu__header-links header-links1">
            <div class="pvu__link-text link-text1">
              Community
            </div>
            <div class="pvu__link-menu link-menu1">
              <a :href="communityBaseUrl + '/welcome'">Welcome</a>
              <a
                :href="communityBaseUrl + '/rules-of-conduct'"
                class="pvu__secondary-link"
                >Rules of Conduct</a
              >
              <a
                :href="communityBaseUrl + '/events'"
                class="pvu__secondary-link"
                >Events and Workshops</a
              >
              <a
                :href="communityBaseUrl + '/contact'"
                class="pvu__secondary-link"
                >Contact Us</a
              >
              <a :href="communityBaseUrl + '/forum'">Forum</a>
              <a :href="communityBaseUrl + '/data-in-action'">Data Spotlight</a>
            </div>
          </div>
        </div>
        <div class="pvu__mobile mobile1">
          <div class="pvu__bars" @click="mobile1menu = true">
            <span></span>
            <span></span>
            <span></span>
          </div>
          <div class="pvu__mobile1-menu" v-if="mobile1menu">
            <div class="pvu__mobile1-close">
              <span @click="mobile1menu = false">x</span>
            </div>
            <div class="pvu__mobile1-section">
              <div class="pvu__mobile1-section-head">
                About
              </div>
              <div>
                <a :href="communityBaseUrl + '/what-is-patentsview'"
                  >What Is PatentsView</a
                >
                <a :href="communityBaseUrl + '/glossary'">Glossary</a>
                <a :href="communityBaseUrl + '/about/terms-privacy'"
                  >Terms of Use and Privacy</a
                >
              </div>
            </div>
            <div class="pvu__mobile1-section">
              <div class="pvu__mobile1-section-head">
                Methods & Sources
              </div>
              <div>
                <a :href="communityBaseUrl + '/disambiguation'"
                  >Disambiguition</a
                >
                <a :href="communityBaseUrl + '/gender-attribution'"
                  >Gender Attributes</a
                >
                <a :href="communityBaseUrl + '/government-interest'"
                  >Government Interests</a
                >
              </div>
            </div>
            <div class="pvu__mobile1-section">
              <div class="pvu__mobile1-section-head">
                Community
              </div>
              <div>
                <a :href="communityBaseUrl + '/welcome'">Welcome</a>
                <a
                  :href="communityBaseUrl + '/rules-of-conduct'"
                  class="pvu__secondary-link"
                  >Rules of Conduct</a
                >
                <a
                  :href="communityBaseUrl + '/events'"
                  class="pvu__secondary-link"
                  >Events and Workshops</a
                >
                <a
                  :href="communityBaseUrl + '/contact'"
                  class="pvu__secondary-link"
                  >Contact Us</a
                >
                <a :href="communityBaseUrl + '/forum'">Forum</a>
                <a :href="communityBaseUrl + '/data-in-action'"
                  >Data Spotlight</a
                >
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- second row -->
    <section class="pvu__header-second">
      <div
        class="pvu__header-menu"
        :class="this.scrollPosY > 45 ? 'longer-second-row' : null"
      >
        <a :href="pvBaseUrl + '/'">
          <div class="pvu__logo">
            <img :src="pv_logo" alt="Logo: USPTO PatentsView" />
          </div>
        </a>
        <div class="pvu__desktop desktop2">
          <div class="pvu__header-links header-links2">
            <div class="pvu__link-text link-text2">
              DATA VISUALIZATION
            </div>
            <div class="pvu__link-menu link-menu2">
              <a :href="pvBaseUrl + '/web/#viz/relationships'">Relationships</a>
              <a :href="pvBaseUrl + '/web/#viz/locations'">Locations</a>
              <a :href="pvBaseUrl + '/web/#viz/comparisons'">Comparisons</a>
            </div>
          </div>
          <div class="pvu__header-links header-links2">
            <div class="pvu__link-text link-text2">
              EXPLORE PATENTS DATA
            </div>
            <div class="pvu__link-menu link-menu2">
              <a :href="pvBaseUrl + '/web/#search&simp=1'">Simple Search</a>
              <a :href="pvBaseUrl + '/web/#search'">Advanced Search</a>
            </div>
          </div>
          <div class="pvu__header-links header-links2">
            <div class="pvu__link-text link-text2">
              DATASETS
            </div>
            <div class="pvu__link-menu link-menu2">
              <a :href="pvBaseUrl + '/query'">Query Builder</a>
              <a
                :href="communityBaseUrl + '/query/data-dictionary'"
                class="pvu__secondary-link"
                >Query Build Data Dictionary</a
              >
              <a
                :href="communityBaseUrl + '/query/builder-faqs'"
                class="pvu__secondary-link"
                >Query Builder FAQs</a
              >
              <a :href="pvBaseUrl + '/download'">Data Download Tables</a>
              <a
                href="https://s3.amazonaws.com/data.patentsview.org/documents/Patents_DB_dictionary_bulk_downloads.xlsx"
                class="pvu__secondary-link"
                >Data Download Data Dictionary</a
              >
            </div>
          </div>
          <div class="pvu__header-links header-links2">
            <div class="pvu__link-text link-text2">
              APIs
            </div>
            <div class="pvu__link-menu link-menu2">
              <a :href="communityBaseUrl + '/apis/purpose'">Purpose</a>
              <a :href="communityBaseUrl + '/apis/api-faqs'">API FAQs</a>
              <a :href="communityBaseUrl + '/apis/api-query-language'"
                >API Query Language</a
              >
              <a :href="communityBaseUrl + '/apis/api-endpoints'"
                >API Endpoints</a
              >
            </div>
          </div>
          <div class="pvu__header-links header-links2 secondary-links">
            <div class="pvu__link-text link-text2">
              ABOUT
            </div>
            <div class="pvu__link-menu link-menu2">
              <a :href="communityBaseUrl + '/what-is-patentsview'"
                >What Is PatentsView</a
              >
              <a :href="communityBaseUrl + '/glossary'">Glossary</a>
              <a :href="communityBaseUrl + '/about/terms-privacy'"
                >Terms of Use and Privacy</a
              >
            </div>
          </div>
          <div class="pvu__header-links header-links2 secondary-links">
            <div class="pvu__link-text link-text2">
              METHODS & SOURCES
            </div>
            <div class="pvu__link-menu link-menu2">
              <a :href="communityBaseUrl + '/disambiguation'">Disambiguition</a>
              <a :href="communityBaseUrl + '/gender-attribution'"
                >Gender Attributes</a
              >
              <a :href="communityBaseUrl + '/government-interest'"
                >Government Interests</a
              >
            </div>
          </div>
          <div class="pvu__header-links header-links2 secondary-links">
            <div class="pvu__link-text link-text2">
              COMMUNITY
            </div>
            <div class="pvu__link-menu link-menu2">
              <a :href="communityBaseUrl + '/welcome'">Welcome</a>
              <a
                :href="communityBaseUrl + '/rules-of-conduct'"
                class="pvu__secondary-link"
                >Rules of Conduct</a
              >
              <a
                :href="communityBaseUrl + '/events'"
                class="pvu__secondary-link"
                >Events and Workshops</a
              >
              <a
                :href="communityBaseUrl + '/contact'"
                class="pvu__secondary-link"
                >Contact Us</a
              >
              <a :href="communityBaseUrl + '/forum'">Forum</a>
              <a :href="communityBaseUrl + '/data-in-action'">Data Spotlight</a>
            </div>
          </div>
        </div>
        <div class="pvu__mobile mobile2">
          <div class="pvu__bars" @click="mobile2menu = true">
            <span></span>
            <span></span>
            <span></span>
          </div>
          <div class="pvu__mobile2-menu" v-if="mobile2menu">
            <div class="pvu__mobile2-close">
              <span @click="mobile2menu = false">x</span>
            </div>
            <div class="pvu__mobile2-grid">
              <div class="pvu__mobile2-section">
                <div class="pvu__mobile2-section-head">
                  DATA VISUALIZATION
                </div>
                <div>
                  <a :href="pvBaseUrl + '/web/#viz/relationships'"
                    >Relationships</a
                  >
                  <a :href="pvBaseUrl + '/web/#viz/locations'">Locations</a>
                  <a :href="pvBaseUrl + '/web/#viz/comparisons'">Comparisons</a>
                </div>
              </div>
              <div class="pvu__mobile2-section">
                <div class="pvu__mobile2-section-head">
                  EXPLORE PATENTS DATA
                </div>
                <div>
                  <a :href="pvBaseUrl + '/web/#search&simp=1'">Simple Search</a>
                  <a :href="pvBaseUrl + '/web/#search'">Advanced Search</a>
                </div>
              </div>
              <div class="pvu__mobile2-section">
                <div class="pvu__mobile2-section-head">
                  DATASETS
                </div>
                <div>
                  <a :href="pvBaseUrl + '/query'">Query Builder</a>
                  <a
                    :href="communityBaseUrl + '/query/data-dictionary'"
                    class="pvu__secondary-link"
                    >Query Build Data Dictionary</a
                  >
                  <a
                    :href="communityBaseUrl + '/query/builder-faqs'"
                    class="pvu__secondary-link"
                    >Query Builder FAQs</a
                  >
                  <a :href="pvBaseUrl + '/download'">Data Download Tables</a>
                  <a
                    href="https://s3.amazonaws.com/data.patentsview.org/documents/Patents_DB_dictionary_bulk_downloads.xlsx"
                    class="pvu__secondary-link"
                    >Data Download Data Dictionary</a
                  >
                </div>
              </div>
              <div class="pvu__mobile2-section">
                <div class="pvu__mobile2-section-head">
                  APIs
                </div>
                <div>
                  <a :href="communityBaseUrl + '/apis/purpose'">Purpose</a>
                  <a :href="communityBaseUrl + '/apis/api-faqs'">API FAQs</a>
                  <a :href="communityBaseUrl + '/apis/api-query-language'"
                    >API Query Language</a
                  >
                  <a :href="communityBaseUrl + '/apis/api-endpoints'"
                    >API Endpoints</a
                  >
                </div>
              </div>
              <div class="pvu__mobile2-section secondary-links">
                <div class="pvu__mobile2-section-head">
                  ABOUT
                </div>
                <div>
                  <a :href="communityBaseUrl + '/what-is-patentsview'"
                    >What Is PatentsView</a
                  >
                  <a :href="communityBaseUrl + '/glossary'">Glossary</a>
                  <a :href="communityBaseUrl + '/about/terms-privacy'"
                    >Terms of Use and Privacy</a
                  >
                </div>
              </div>
              <div class="pvu__mobile2-section secondary-links">
                <div class="pvu__mobile2-section-head">
                  METHODS & SOURCES
                </div>
                <div>
                  <a :href="communityBaseUrl + '/disambiguation'"
                    >Disambiguition</a
                  >
                  <a :href="communityBaseUrl + '/gender-attribution'"
                    >Gender Attributes</a
                  >
                  <a :href="communityBaseUrl + '/government-interest'"
                    >Government Interests</a
                  >
                </div>
              </div>
              <div class="pvu__mobile2-section secondary-links">
                <div class="pvu__mobile2-section-head">
                  COMMUNITY
                </div>
                <div>
                  <a :href="communityBaseUrl + '/welcome'">Welcome</a>
                  <a
                    :href="communityBaseUrl + '/rules-of-conduct'"
                    class="pvu__secondary-link"
                    >Rules of Conduct</a
                  >
                  <a
                    :href="communityBaseUrl + '/events'"
                    class="pvu__secondary-link"
                    >Events and Workshops</a
                  >
                  <a
                    :href="communityBaseUrl + '/contact'"
                    class="pvu__secondary-link"
                    >Contact Us</a
                  >
                  <a :href="communityBaseUrl + '/forum'">Forum</a>
                  <a :href="communityBaseUrl + '/data-in-action'"
                    >Data Spotlight</a
                  >
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </header>
</template>

<script>
import pv_logo from "../img/pv-header-logo.png";
import baseUrl from "../baseUrl.js";

export default {
  data() {
    return {
      pv_logo,
      scrollPosY: 0,
      mobile1menu: false,
      mobile2menu: false,
      communityBaseUrl: baseUrl(window.location.hostname).community,
      pvBaseUrl: baseUrl(window.location.hostname).pv,
    };
  },
  mounted() {
    window.addEventListener("scroll", () => {
      this.scrollPosY = window.scrollY;
    });
    document.body.style.height = "auto";
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&display=swap");

.pvu__header * {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-family: "Open Sans", sans-serif;
}

.pvu__header {
  position: sticky;
  position: -webkit-sticky;
  top: -45px;
  z-index: 999;
}

.pvu__header .pvu__header-first {
  background-color: #d0dded;
}

.pvu__header .pvu__header-menu {
  max-width: 930px;
  padding: 0 30px;
  margin: 0 auto;
  box-sizing: content-box;
}

.pvu__header-first .pvu__header-menu {
  height: 45px;
}

.pvu__header .pvu__header-second {
  background-color: #4f5f6f;
}

.pvu__header-second .pvu__header-menu {
  height: 70px;
}

.pvu__logo {
  float: left;
  height: 100%;
  display: flex;
  align-items: center;
}
.pvu__logo img {
  max-width: 221px;
  /* animation-duration: 200ms;
  animation-name: shrink-back; */
}
.longer-second-row .pvu__logo img {
  max-width: 120px;
  /* animation-duration: 200ms;
  animation-name: shrink; */
}
/* @keyframes shrink {
  from {
    max-width: 221px;
  }
  to {
    max-width: 120px;
  }
}
@keyframes shrink-back {
  from {
    max-width: 120px;
  }
  to {
    max-width: 221px;
  }
} */

.pvu__desktop {
  float: right;
  display: flex;
  height: 100%;
  width: 100%;
  justify-content: space-between;
  align-items: center;
}
@media (max-width: 475px) {
  .desktop1 {
    display: none;
  }
}
.desktop1 {
  max-width: 380px;
}
@media (max-width: 950px) {
  .desktop2 {
    display: none;
  }
}
.desktop2 {
  max-width: 600px;
  /* animation-duration: 200ms;
  animation-name: expand-back; */
}
.longer-second-row .desktop2 {
  max-width: 750px;
  /* animation-duration: 200ms;
  animation-name: expand; */
}
/* @keyframes expand {
  from {
    max-width: 600px;
  }
  to {
    max-width: 750px;
  }
}
@keyframes expand-back {
  from {
    max-width: 750px;
  }
  to {
    max-width: 600px;
  }
} */

.pvu__header-links {
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  height: 100%;
  line-height: 24px;
  font-size: 14px;
  cursor: default;
  /* animation-duration: 200ms;
  animation-name: shrink-font-back; */
}
.header-links1 {
  color: #7c8c9f;
}
.header-links2 {
  color: #f1d673;
}
.longer-second-row .pvu__header-links {
  font-size: 12px;
  /* animation-duration: 200ms;
  animation-name: shrink-font; */
}
/* @keyframes shrink-font {
  from {
    font-size: 14px;
  }
  to {
    font-size: 12px;
  }
}
@keyframes shrink-font-back {
  from {
    font-size: 12px;
  }
  to {
    font-size: 14px;
  }
} */

.secondary-links {
  display: none;
  /* animation-duration: 200ms; */
}
.longer-second-row .secondary-links {
  display: flex;
  /* animation-duration: 200ms;
  animation-name: shift; */
}
/* @keyframes shift {
  from {
    transform: translateX(-150px);
    display: none;
  }
  to {
    transform: translateX(0);
    display: flex;
  }
} */

.pvu__link-text {
  padding: 0 20px;
}
.longer-second-row .pvu__link-text {
  padding: 0 10px;
}

.pvu__link-menu {
  display: none;
  position: absolute;
  right: 0;
  left: auto;
  padding: 10px 0;
}
.link-menu1 {
  top: 45px;
  background-color: black;
}
.link-menu1 a {
  color: white;
}
.link-menu2 {
  top: 70px;
  background-color: #f5e095;
}
.link-menu2 a {
  color: #444444;
}
.link-menu2 a:not(:first-child) {
  margin-top: 10px;
}

.pvu__link-menu a {
  padding: 0 20px;
  line-height: 35px;
  display: block;
  text-decoration: none;
  white-space: nowrap;
}
.link-menu1 a:hover {
  background-color: #444444;
}
.link-menu2 a:hover {
  background-color: #f1d673;
  color: black;
}
a.pvu__secondary-link {
  padding-left: 40px;
}

.pvu__header-links:hover .pvu__link-text {
  height: 100%;
  display: flex;
  align-items: center;
}
.pvu__header-links:hover .link-text1 {
  background-color: black;
  color: white;
}
.pvu__header-links:hover .link-text2 {
  background-color: #f5e095;
  color: black;
}

.pvu__header-links:hover .pvu__link-menu {
  display: block;
  z-index: 1;
}

.pvu__bars span {
  display: block;
  width: 22px;
  height: 2px;
  border-radius: 1px;
  display: block;
}
.mobile1 .pvu__bars span {
  background-color: #4f5f6f;
}
.mobile2 .pvu__bars span {
  background-color: white;
}

.pvu__bars span:not(:first-child) {
  margin-top: 4px;
}

.pvu__mobile {
  display: none;
  height: 100%;
  float: right;
  align-items: center;
  cursor: pointer;
}
@media (max-width: 475px) {
  .mobile1 {
    display: flex;
  }
}
@media (max-width: 950px) {
  .mobile2 {
    display: flex;
  }
}

.pvu__mobile1-menu {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background-color: black;
  color: white;
  padding: 20px 0;
  cursor: default;
  font-size: 14px;
}

.pvu__mobile1-menu .pvu__secondary-link {
  padding-left: 40px;
}

.pvu__mobile1-menu a {
  text-decoration: none;
  color: white;
  display: block;
  padding-left: 20px;
  margin: 5px 0;
}

.pvu__mobile1-menu a:hover {
  background-color: #444444;
}

.pvu__mobile1-section {
  margin: 20px 0;
}

.pvu__mobile1-section-head {
  font-weight: bold;
  padding-left: 20px;
  margin-bottom: 10px;
}

.pvu__mobile1-close {
  text-align: right;
  font-size: 20px;
  font-weight: bold;
  padding-right: 20px;
}

.pvu__mobile1-close span {
  cursor: pointer;
}

.pvu__mobile2-menu {
  position: fixed;
  top: 0;
  left: 0;
  background-color: #f5e095;
  width: 100%;
  cursor: default;
  font-size: 14px;
  max-height: 80vh;
  overflow: auto;
}

.pvu__mobile2-grid {
  padding: 20px 40px;
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, max-content));
  gap: 20px;
}

.pvu__mobile2-menu a {
  text-decoration: none;
  color: #444444;
  display: block;
  margin: 5px 0;
}

.pvu__mobile2-menu a:hover {
  background-color: #f1d673;
  color: black;
}

.longer-second-row .pvu__mobile2-menu .secondary-links {
  display: block;
}

.pvu__mobile2-section-head {
  font-weight: bold;
  margin-bottom: 10px;
  color: #5d5d5d;
}

.pvu__mobile2-close {
  margin-top: 20px;
  text-align: right;
  font-size: 20px;
  font-weight: bold;
  padding-right: 20px;
}

.pvu__mobile2-close span {
  cursor: pointer;
  color: #5d5d5d;
}
</style>
