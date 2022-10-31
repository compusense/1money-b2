<template>
  <q-page class="column flex-center">
    <q-header reveal elevated class="bg-primary text-white">
      <q-toolbar>
        <q-toolbar-title class="text-bold">
          <q-avatar>
            <img alt="1Money logo" src="~assets/one_logo.svg" />
          </q-avatar>
          1Money
        </q-toolbar-title>
      </q-toolbar>
    </q-header>
    <q-parallax
      style="min-height: 610px"
      src="https://img.freepik.com/free-photo/closeup-diverse-people-joining-their-hands_53876-96081.jpg?w=1380&t=st=1667127142~exp=1667127742~hmac=f37f4278d2d346548604bc1226e3edabcd2253eeed61ee5275dde06828fc07cc"
    >
      <h1 class="text-white text-bold">Connect to Thrive</h1>

      <q-page-container
        ><div class="q-pa-lg">
          <q-card style="max-width: 400px">
            <q-skeleton height="00px" square />

            <div id="q-app" style="min-height: 60vh">
              <div class="q-pa-lg">
                <q-form @submit="onSubmit" class="q-gutter-md">
                  <h6 class="text-primary column flex-center">
                    Become a Part of Something Amazing
                  </h6>
                  <q-input
                    outlined
                    v-model="name"
                    label="First name"
                    hint="Names as they appear on ID"
                  ></q-input>

                  <q-input
                    outlined
                    v-model="name"
                    label="Last name"
                    hint="Names as they appear on ID"
                  ></q-input>

                  <div style="min-width: 350px">
                    <q-input
                      filled
                      v-model="date"
                      mask="date"
                      :rules="['date']"
                      label="Select Your Birthday"
                    >
                      <template v-slot:append>
                        <q-icon name="event" class="cursor-pointer">
                          <q-popup-proxy
                            cover
                            transition-show="scale"
                            transition-hide="scale"
                          >
                            <q-date v-model="date">
                              <div class="row items-center justify-end">
                                <q-btn
                                  v-close-popup
                                  label="Close"
                                  color="primary"
                                  flat
                                />
                              </div>
                            </q-date>
                          </q-popup-proxy>
                        </q-icon>
                      </template>
                    </q-input>
                  </div>

                  <q-input
                    outlined
                    type="Number"
                    v-model="number"
                    label="ID Number/Omang"
                    hint="ID Number as printed in your ID card"
                  ></q-input>

                  <div></div>

                  <div class="q-ml-xs q-gutter-md row flex-center">
                    <br />

                    <q-btn label="Home" type="submit" color="secondary"></q-btn>

                    <q-btn
                      label="Next"
                      type="submit"
                      color="positive"
                      q-pl-lg
                    ></q-btn>
                  </div>
                </q-form>
              </div>
            </div>
          </q-card>
        </div>
      </q-page-container>
    </q-parallax>
    <q-footer reveal elevated class="bg-primary text-white text-italic">
      <q-toolbar> "Value in everything" </q-toolbar>
    </q-footer>
  </q-page>
</template>

<script>
import { defineComponent, ref } from 'vue';
import EssentialLink from 'components/EssentialLink.vue';

const linksList = [
  {
    title: 'Send Cash',
    caption: 'Send money with ease',
    icon: 'school',
    link: 'https://quasar.dev',
  },
  {
    title: 'Withdraw Cash',
    caption: 'Access your money',
    icon: 'code',
    link: 'https://github.com/quasarframework',
  },
  {
    title: 'Deposit Cash',
    caption: 'Add money to your account',
    icon: 'chat',
    link: 'https://chat.quasar.dev',
  },
  {
    title: 'Purchase',
    caption: 'Buy and pay with 1Money',
    icon: 'record_voice_over',
    link: 'https://forum.quasar.dev',
  },
  {
    title: 'Payments',
    caption: 'Make monthly payments',
    icon: 'rss_feed',
    link: 'https://twitter.quasar.dev',
  },
  {
    title: 'Convert',
    caption: 'Convert airtime, cash and electricity',
    icon: 'public',
    link: 'https://facebook.quasar.dev',
  },
  {
    title: 'Account Management',
    caption: 'Manage your accounts',
    icon: 'favorite',
    link: 'https://awesome.quasar.dev',
  },
  {
    title: 'Rewards',
    caption: 'Get insights on your rewards',
    icon: 'record_voice_over',
    link: 'https://awesome.quasar.dev',
  },
];
</script>
