<template>
  <card>
    <b-row align-v="center" slot="header" >
      <b-col cols="8">
        <h3 class="mb-0">Профиль</h3>
      </b-col>
      <b-col cols="4" class="text-right">
        <a href="#!" class="btn btn-sm btn-primary">Сохранить</a>
      </b-col>
    </b-row>

    <b-form @submit.prevent="updateProfile">
      <h6 class="heading-small text-muted mb-4">Информация о пользователе</h6>

      <div class="pl-lg-4">
        <b-row>
          <b-col lg="6">
            <base-input
              type="text"
              label="Имя пользователя"
              placeholder="Username"
              v-model="user.username"
            >
            </base-input>
          </b-col>
          <b-col lg="6">
            <base-input
              type="email"
              label="Почта"
              placeholder="Почта"
              v-model="user.email"
            >
            </base-input>
          </b-col>
          <b-col lg="6">
            <base-input
              type="password"
              label="Пароль"
              placeholder="Пароль"
              v-model="user.password"
            >
            </base-input>
            
          </b-col>
        </b-row>
        <!-- <b-row >
          <b-col lg="6">
            <base-input
              type="text"
              label="Имя"
              placeholder="First Name"
              v-model="user.firstName"
            >
            </base-input>
          </b-col>
          <b-col lg="6">
            <base-input
              type="text"
              label="Фамилия"
              placeholder="Last Name"
              v-model="user.lastName"
            >
            </base-input>
          </b-col>
        </b-row> -->
      </div>
      <!-- <hr class="my-4"> -->

      <!-- Address -->
      <!-- <h6 class="heading-small text-muted mb-4">Contact information</h6> -->

      <!-- <div class="pl-lg-4">
        <b-row>
          <b-col md="12">
            <base-input
              type="text"
              label="Address"
              placeholder="Home Address"
              v-model="user.address"
            >
            </base-input>
          </b-col>
        </b-row>
        <b-row>
          <b-col lg="4">
            <base-input
              type="text"
              label="City"
              placeholder="City"
              v-model="user.city"
            >
            </base-input>
          </b-col>
          <b-col lg="4">
            <base-input
              type="text"
              label="Country"
              placeholder="Country"
              v-model="user.country"
            >
            </base-input>
          </b-col>
          <b-col lg="4">
            <base-input
              label="Postal Code"
              placeholder="ZIP Code"
              v-model="user.postalCode"
            >
            </base-input>
          </b-col>
        </b-row>
      </div> -->

      <hr class="my-4">
      <h6 class="heading-small text-muted mb-4">Информация с лк бонча</h6>
      <div class="pl-lg-4">
        <b-row>
          <b-col lg="6">
            <base-input
              type="text"
              label="Имя"
              placeholder="Николай"
              v-model="user.firstName"
            >
            </base-input>
          </b-col>
          <b-col lg="6">
            <base-input
              type="email"
              label="Фамилия"
              placeholder="Фамилия"
              v-model="user.lastName"
            >
            </base-input>
          </b-col>
          <b-col lg="6">
            <base-input
              type="email"
              label="Почта"
              placeholder="Почта"
              v-model="user.email"
            >
            </base-input>
          </b-col>
          <b-col lg="6">
            <base-input
              type="password"
              label="Пароль"
              placeholder="Пароль"
              v-model="user.password"
            >
            </base-input>
            
          </b-col>
        </b-row>
      </div>


      <hr class="my-4">
      <h6 class="heading-small text-muted mb-4">Данные сервиса бонча</h6>
      <div class="pl-lg-4">
        <b-row>
          <b-col lg="6">
            <base-input
              type="login"
              label="Логин"
              placeholder="Логин"
              v-model="user.email"
            >
            </base-input>
          </b-col>
          <b-col lg="6">
            <base-input
              type="password"
              label="Пароль"
              placeholder="Пароль"
              v-model="user.password"
            >
            </base-input>
          </b-col>
        </b-row>
      </div>
      <!-- <div class="pl-lg-4"> -->
        <!-- <b-form-group label="About Me" label-class="form-control-label" class="mb-0" label-for="about-form-textaria"> -->
         <!--  <label class="form-control-label">About Me</label> -->
          <!-- <b-form-textarea rows="4" value="A beautiful premium dashboard for BootstrapVue." id="about-form-textaria" placeholder="A few words about you ..."></b-form-textarea> -->
        <!-- </b-form-group> -->
      <!-- </div> -->

    </b-form>
  </card>
</template>
<script>
export default {
  data() {
    return {
      user: {
        company: 'Creative Code Inc.',
        username: 'Bit',
        email: '',
        firstName: 'Николай',
        lastName: 'Никоноров',
        address: 'Bld Mihail Kogalniceanu, nr. 8 Bl 1, Sc 1, Ap 09',
        city: '',
        country: 'Russia',
        postalCode: '',
        password: '',
        aboutMe: `Lamborghini Mercy, Your chick she so thirsty, I'm in that two seat Lambo.`
      }
    };
  },
  methods: {
    updateProfile() {
      alert('Your data: ' + JSON.stringify(this.user));
    }
  }
};
</script>
<style></style>
