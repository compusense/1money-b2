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
      src="https://img.freepik.com/free-photo/cropped-shot-african-american-businessman-paying-with-credit-card-online_273609-9075.jpg?w=1060&t=st=1667086881~exp=1667087481~hmac=23de91f9d86fb78d0195bb7446d9a4b85e28852358dd952119f0248e15a86a0b"
    >
      <h1 class="text-white text-bold">Beyond Powerful</h1>

      <q-page-container
        ><div class="q-pa-lg">
          <q-card style="min-width: 300px">
            <q-skeleton height="00px" square />

            <div id="q-app" style="min-height: 60vh">
              <div class="q-pa-lg">
                <q-form @submit="onSubmit" class="q-gutter-lg">
                  <img
                    alt="1Money logo"
                    src="~assets/quasar-logo-vertical.svg"
                    style="width: 250px; height: 190px"
                  />
                  <q-input
                    outlined
                    v-model="number"
                    label="Mobile Number"
                    hint="Cellphone Number"
                    prefix="267"
                  ></q-input>

                  <q-input
                    outlined
                    type="Secret Code"
                    v-model="pin"
                    label="Secret Code"
                    hint="5 Digit PIN"
                  ></q-input>

                  <div></div>

                  <div class="q-ml-lg q-gutter-lg flex-center">
                    <br />
                    <div class="text-primary text-bold">
                      I don't remember my PIN
                    </div>

                    <q-btn
                      outline
                      label="Sign In"
                      type="submit"
                      color="secondary"
                    ></q-btn>

                    <q-btn
                      outline
                      label="Sign Up"
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
