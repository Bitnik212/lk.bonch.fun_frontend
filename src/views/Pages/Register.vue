<template>
  <div>
    <!-- Header -->
    <div class="header bg-gray py-7 py-lg-5 pt-lg-9">
      <b-container class="container">
        <div class="header-body text-center mb-5">
          <b-row class="justify-content-center">
            <b-col xl="5" lg="6" md="8" class="px-5">
              <h1 class="text-white">Создай свой аккаунт</h1>
              <p class="text-lead text-white">Блин, чел, ты реально это хочешь ?</p>
            </b-col>
          </b-row>
        </div>
      </b-container>
      <div class="separator separator-bottom separator-skew zindex-100">
        <svg x="0" y="0" viewBox="0 0 2560 100" preserveAspectRatio="none" version="1.1"
             xmlns="http://www.w3.org/2000/svg">
          <polygon class="fill-default" points="2560 0 2560 100 0 100"></polygon>
        </svg>
      </div>
    </div>
    <!-- Page content -->
    <b-container class=" col-12 col-sm-10 col-md-10">
      <!-- Table -->
      <b-row class="justify-content-center">
        <b-col lg="7" md="10" sm="10">
          <b-card no-body class="bg-secondary border-0 p-3 p-lg-5 p-xl-5 p-md-4 p-sm-3 ">
            <!-- <b-card-header class="bg-transparent pb-5">
              <div class="text-muted text-center mt-2 mb-4"><small>Зарегайся через</small></div>
              <div class="text-center">
                <a href="#" class="btn btn-neutral btn-icon mr-4">
                  <span class="btn-inner--icon"><img src="img/icons/common/github.svg"></span>
                  <span class="btn-inner--text">Github</span>
                </a>
                <a href="#" class="btn btn-neutral btn-icon">
                  <span class="btn-inner--icon"><img src="img/icons/common/google.svg"></span>
                  <span class="btn-inner--text">Google</span>
                </a>
              </div>
            </b-card-header> -->

            <b-tabs pills class="  ">
              <b-tab active  class="">
                <template v-slot:title class="">
                  Данные сервиса
                </template>
                  <div class="text-left text-muted my-4 ">
                    <small>Введи свои данные для этого лк, чтобы ты мог не париться и забыть данные от лк бонча</small>
                  </div>
                    <validation-observer v-slot="{handleSubmit}" ref="formValidator">
                      <b-form role="form" @submit.prevent="handleSubmit(onSubmit)">
                        <!-- <small class="">Именно так я буду к тебе обращаться</small> -->
                        <base-input alternative
                                    class="mb-3"
                                    prepend-icon="ni ni-circle-08"
                                    placeholder="Именно так я буду к тебе обращаться"
                                    name="Name"
                                    :rules="{required: true}"
                                    v-model="model.name">
                        </base-input>

                        <base-input alternative
                                    class="mb-3"
                                    prepend-icon="ni ni-email-83"
                                    placeholder="А на эту почту я, наверное, буду тебе писать"
                                    name="Email"
                                    :rules="{required: true, email: true}"
                                    v-model="model.email">
                        </base-input>

                        <base-input alternative
                                    class="mb-3"
                                    prepend-icon="ni ni-lock-circle-open"
                                    placeholder="Просто введи свой чертов пароль"
                                    type="password"
                                    name="Password"
                                    :rules="{required: true, min: 6}"
                                    v-model="model.password">
                        </base-input>
                        <div class="text-muted font-italic">
                          <small>Толщина пароля: 
                            <span
                            class="text-success font-weight-700"
                            >Сильная</span>
                          </small>
                        </div>
                      </b-form>
                    </validation-observer>
              </b-tab>

              <b-tab>
                <template v-slot:title>
                   Данные лк бонча
                </template>
                <div class="text-left text-muted my-4">
                  <small>Введи свои данные для лк бонча, чтобы я мог отчислить тебя. Ой. То есть смог войти в твой лк и работать с ним через мое апи, которе я, конечно, тебе не покажу)))) </small>
                </div>
                <validation-observer v-slot="{handleSubmit}" ref="formValidator">
                  <b-form role="form" @submit.prevent="handleSubmit(onSubmit)">
                    <base-input alternative
                                class="mb-3"
                                prepend-icon="ni ni-email-83"
                                placeholder="Здесь введи почту(логин) лк бонча"
                                name="Email"
                                :rules="{required: true, email: true}"
                                v-model="model.email">
                    </base-input>

                    <base-input alternative
                                class="mb-3"
                                prepend-icon="ni ni-lock-circle-open"
                                placeholder="Просто введи свой чертов пароль, я всё равно узнаю его))))"
                                type="password"
                                name="Password"
                                :rules="{required: true, min: 6}"
                                v-model="model.password">
                    </base-input>
                    <!-- <div class="text-muted font-italic">
                      <small>Толщина пароля: 
                        <span
                        class="text-success font-weight-700"
                        >Сильная</span>
                      </small>
                    </div> -->
                    <b-row class=" my-4">
                      <b-col cols="12">
                        <base-input :rules="{ required: { allowFalse: false } }" name=Privacy Policy>
                          <b-form-checkbox v-model="model.agree">
                            <span class="text-muted">Я согласен(на) с <a href="#!">политикой конфиденциальности</a></span>
                          </b-form-checkbox>
                        </base-input>
                      </b-col>
                    </b-row>
                    <div class="text-center">
                      <b-button type="submit" variant="primary" class="mt-4">Создать аккаунт</b-button>
                    </div>
                  </b-form>
                </validation-observer>
                <!-- <p class="p-3">Cosby sweater eu banh mi, qui irure terry richardson ex squid. Aliquip placeat salvia cillum iphone. Seitan aliquip quis cardigan american apparel, butcher voluptate nisi qui.</p> -->
              </b-tab>

              <!-- <b-tab>
                <template v-slot:title>
                  <i class="ni ni-calendar-grid-58 mr-2"></i> Messages
                </template>
                <p class="p-3">Raw denim you probably haven't heard of them jean shorts Austin. Nesciunt tofu stumptown aliqua, retro synth master cleanse. Mustache cliche tempor, williamsburg carles vegan helvetica. Reprehenderit butcher retro keffiyeh dreamcatcher synth.</p>
              </b-tab> -->
          </b-tabs>

          </b-card>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>
<script>

  export default {
    name: 'register',
    data() {
      return {
        model: {
          name: '',
          email: '',
          password: '',
          agree: false
        }
      }
    },
    methods: {
      onSubmit() {
        // this will be called only after form is valid. You can do an api call here to register users
      }
    }

  };
</script>
<style scoped>
  
</style>
