<template>
  <v-footer
    id="footer"
    class="footer d-flex flex-column justify-space-between align-center"
  >
    <div class="footer-content d-flex flex-column justify-space-between">
      <div>
        <v-row class="subscribe-panel ma-0">
          <v-row class="subscribe-text-panel col-12 px-0 ma-0">
            <h2 class="subscribe-title col-6 px-0">
              Subscribe to our Newsletter
            </h2>
            <p class="subscribe-description col-6 pr-0">
              The fascinating world of diamonds presented by Royal Coster.
              Products, tours and news. We won't spam your inbox.
            </p>
          </v-row>
          <v-row class="email-subscribe-panel d-flex ma-0 mt-10 col-12 pa-0">
            <input
              type="email"
              class="form-control input-email col-md-10 col-sm-9 mr-1"
              placeholder="Email Address"
              v-model="email"
            />
            <v-btn tile color="grey darken-4 white--text btn-subscribe" class="py-6">
              SUBSCRIBE
            </v-btn>
          </v-row>
        </v-row>
      </div>
      <div>
        <div
          class="contact-footer d-flex flex-column justify-space-between align-center mt-10"
        >
          <img
            src="~/assets/img/logo 3.png"
            alt="footer-logo"
            class="footer-logo"
          />
          <v-row class="footer-content-panel col-12 mt-10 px-0">
            <v-col
              lg="4"
              md="4"
              sm="12"
              col="12"
              class="quick-link-panel px-0 text-md-left text-center"
            >
              <h4>Quick links</h4>
              <v-row class="mx-0 mt-3">
                <v-col cols="6" class="px-0">
                  <NuxtLink
                    v-for="(item, index) in link1"
                    :key="index"
                    :to="item.url"
                    class="d-block quick-link mt-3"
                  >
                    {{ item.title }}
                  </NuxtLink>
                </v-col>
                <v-col cols="6">
                  <NuxtLink
                    v-for="(item, index) in link2"
                    :key="index"
                    :to="item.url"
                    class="d-block quick-link mt-3"
                  >
                    {{ item.title }}
                  </NuxtLink></v-col
                >
              </v-row>
            </v-col>
            <v-col
              lg="4"
              md="4"
              sm="12"
              col="12"
              color="black"
              class="btn-group"
            >
              <v-btn outlined class="px-7 py-4 mx-auto text-uppercase d-block"
                >Online Consultation</v-btn
              >
              <v-btn
                outlined
                class="px-7 py-4 mx-auto text-uppercase d-block mt-5"
                >Book an Appoinment</v-btn
              >
            </v-col>
            <v-col
              lg="4"
              md="4"
              sm="12"
              col="12"
              class="follow-us-panel text-md-right text-center px-0"
            >
              <h4 class="">Follow Us</h4>
              <p class="mt-4 text-decoration-underline">@royalcosterdiamonds</p>
              <div class="social-link-panel mt-14">
                <NuxtLink class="social-link text-decoration-none ml-6" to="#">
                  <v-icon>mdi-instagram</v-icon>
                </NuxtLink>
                <NuxtLink class="social-link text-decoration-none ml-6" to="#">
                  <v-icon>mdi-facebook</v-icon>
                </NuxtLink>
                <NuxtLink class="social-link text-decoration-none ml-6" to="#">
                  <v-icon>mdi-youtube</v-icon>
                </NuxtLink>
                <NuxtLink class="social-link text-decoration-none ml-6" to="#">
                  <v-icon>mdi-twitter</v-icon>
                </NuxtLink>
                <NuxtLink class="social-link text-decoration-none ml-6" to="#">
                  <v-icon>mdi-pinterest</v-icon>
                </NuxtLink>
              </div>
            </v-col>
          </v-row>
          <v-row class="copyright-panel col-12 mt-8 mb-0 px-0">
            <v-col md="6" cols="12" class="text-uppercase px-0 text-md-left text-center"
              >© 2020 Royal Coster Diamonds - All rights reserved</v-col
            >
            <v-col md="6" cols="12" class="text-md-right text-center px-0">
              <NuxtLink
                to="#"
                class="text-uppercase text-decoration-none black--text"
                >Privacy Policy</NuxtLink
              >
              <NuxtLink
                to="#"
                class="text-uppercase ml-10 text-decoration-none black--text"
                >Cookies</NuxtLink
              >
              <NuxtLink
                to="#"
                class="text-uppercase ml-10 text-decoration-none black--text"
                >Terms</NuxtLink
              >
            </v-col>
          </v-row>
        </div>
      </div>
    </div>
    <div class="blur-pink-area" />
    <div class="blur-blue-area" />
  </v-footer>
</template>

<script>
export default {
  data: () => ({
    email: "",
    link1: [
      { title: "HOME", url: "#" },
      { title: "ABOUT", url: "#" },
      { title: "JEWELRY", url: "#" }
    ],
    link2: [
      { title: "CONTACT", url: "#" },
      { title: "COLLECTION", url: "#" },
      { title: "LOGIN", url: "#" }
    ]
  })
};
</script>

<style>
#footer {
  position: relative;
  height: 100vh;
  width: 100%;
  background: linear-gradient(180deg, rgba(255, 255, 255, 0) 0%, #e5d7bf 100%);
}
.footer-content {
  position: relative;
  z-index: 10;
  height: 100%;
  width: 80%;
}
.subscribe-title {
  font-family: Canela, sans-serif;
  font-style: normal;
  font-weight: normal;
  font-size: 72px;
  line-height: 78px;
  color: #000000;
}
.subscribe-description {
  font-family: Montserrat, sans-serif;
  font-style: normal;
  font-weight: 300;
  font-size: 24px;
  line-height: 36px;
}
.email-subscribe-panel * {
  font-size: 20px;
}
.email-subscribe-panel .input-email {
  background: #ffffff;
  border: 1px solid rgba(0, 0, 0, 0.1);
  box-sizing: border-box;
  box-shadow: 2px 4px 30px rgba(0, 0, 0, 0.06);
  outline: 0;
  height: 70px;
}
.email-subscribe-panel button {
  font-family: Montserrat;
  font-style: normal;
  font-weight: 500;
  font-size: 20px;
  line-height: 24px;
  text-transform: uppercase;
  color: #ffffff;
  height: 70px !important;
  border-radius: 0;
  flex: 1;
}
.quick-link-panel h4 {
  font-family: Canela, sans-serif;
  font-style: normal;
  font-weight: normal;
  font-size: 24px;
  line-height: 24px;
  color: #000000;
}
.quick-link-panel .quick-link {
  outline: none;
  text-decoration: none;
  font-family: Montserrat, sans-serif;
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  line-height: 17px;
  text-transform: uppercase;
  color: #000000;
}
.follow-us-panel h4,
.follow-us-panel p {
  font-family: Canela, sans-serif;
  font-style: normal;
  font-weight: normal;
  font-size: 24px;
  line-height: 27px;
  color: #000000;
}
.footer-content-panel .btn-group > * {
  height: auto !important;
  border-radius: 0;
  font-family: Montserrat, sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 20px;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  color: #000000;
}
.follow-us-panel .social-link i {
  font-size: 30px;
}
#footer .blur-pink-area {
  position: absolute;
  width: 40vw;
  height: 40vw;
  top: -20%;
  right: 45%;
  background: #fad3da;
  opacity: 0.7;
  filter: blur(300px);
  z-index: 1;
}
#footer .blur-blue-area {
  position: absolute;
  width: 25vw;
  height: 25vw;
  top: 5%;
  left: 55%;
  background: #13439b;
  opacity: 0.3;
  filter: blur(300px);
  z-index: 1;
}

.copyright-panel * {
  font-family: Montserrat, sans-serif;
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  line-height: 17px;
  text-transform: uppercase;
  color: #000000;
}

@media (max-width: 1114px) {
  #footer {
    height: auto;
  }
  .subscribe-title {
    font-size: 50px;
  }
  .subscribe-description {
    font-size: 18px;
  }
  .email-subscribe-panel * {
    font-size: 16px;
  }
}
@media (max-width: 768px) {
  .subscribe-title {
    font-size: 40px;
  }
  .subscribe-description {
    font-size: 12px;
  }
  .email-subscribe-panel .input-email,
  .email-subscribe-panel .btn-subscribe {
    height: 55px !important;
  }
}
</style>
