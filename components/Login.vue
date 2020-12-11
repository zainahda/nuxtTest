<template>
  <div>
    <b-card no-body class="overflow-hidden" style="max-width: 1440px;">
    <b-row no-gutters>
      <b-col class="image" md="6">
        <b-card-img src="../assets/logo.png" alt="Image" class="rounded-0"></b-card-img>
        <h1 class="text">travvago</h1>
      </b-col>
      <b-col md="6">
        <b-card-body >
          <h1 class="title">Welcome to <span>Travvago</span></h1>
          <b-card-text> 
          <!-- form login start -->
          <div class="form-group">
            <input
              type="email"
              class="form-control form-control-user"
              id="exampleInputEmail"
              aria-describedby="emailHelp"
              placeholder="Enter Email Address..."
              v-model="login.email"
            />
          </div>
          <div class="form-group">
            <input
              type="password"
              class="form-control form-control-user"
              id="exampleInputPassword"
              placeholder="Password"
              v-model="login.password"
            />
          </div>
          <div class="form-group">
            <div class="custom-control custom-checkbox small">
              <input
                type="checkbox"
                class="custom-control-input"
                id="customCheck"
              />
              <label class="custom-control-label" for="customCheck"
                >Remember Me</label
              >
            </div>
          </div>
          <a
            href="javascript:void(0)"
            @click="submit"
            class="btn btn-primary btn-user btn-block"
          >
            Login
          </a>
          </b-card-text>
        </b-card-body>
      </b-col>
    </b-row>
  </b-card>
        <!-- <div class="form-container  ml-auto mr-auto">
        <b-form>
          <h6>Enter your email for<span> Login</span></h6>
          <b-form-group
            id="input-group-1"
            label="Email address:"
            label-for="input-1"
          >
            <b-form-input
              id="input-1"
              type="email"
              required
              placeholder="Your email"
              v-model="auth.email"
            ></b-form-input>
          </b-form-group>

          <b-form-group id="input-group-2" label="Password:" label-for="input-2">
            <b-form-input
              id="input-2"
              placeholder="Password"
              v-model="auth.password"
              required
            ></b-form-input>
          </b-form-group>

          <b-btn-group inline >
          <nuxt-link to=""
          class="link"> Forgot Password?
          </nuxt-link>
          <nuxt-link href="javascript:void(0)" @click="submit" type="login" class="button-login" >Login</nuxt-link>
          </b-btn-group>
          <br>
          <nuxt-link to="/">
          <b-button class="button-home col-lg-12  mt-3 ml-auto mr-auto" type="home">Back to Home</b-button>
          </nuxt-link>
        </b-form>
      </div>
      
            form login end -->
        <!-- form sign up start
            <div>
            <b-form>
              <h6>Enter your data for<span> Sign up</span></h6>
              <b-form-group
                id="input-group-1"
                label="Email address:"
                label-for="input-1"
              >
                <b-form-input
                  id="input-1"
                  v-model="form.email"
                  type="email"
                  required
                  placeholder="Email"
                ></b-form-input>
              </b-form-group>

              <b-form-group
                id="input-group-2"
                label="Password:"
                label-for="input-2"
              >
                <b-form-input
                  id="input-2"
                  v-model="auth.password"
                  required
                  placeholder="Password"
                ></b-form-input>
              </b-form-group>

              <b-form-group
                id="input-group-2"
                label="Confirm:"
                label-for="input-2"
              >
                <b-form-input
                  id="input-2"
                  v-model="auth.password"
                  required
                  placeholder="Enter password"
                ></b-form-input>
              </b-form-group>

              <b-button class="button-signup" type="submit">Sign up</b-button>
              <nuxt-link to="/home">
                <b-button
                  class="button-home col-lg-12 mt-3 ml-auto mr-auto"
                  type="home"
                  >Back to Home</b-button
                >
              </nuxt-link>
            </b-form>
          </div> -->
  </div>
</template>

<script>
export default {
  auth: false, //middleware ga jalan
  data() {
    return {
      //var input
      login: {
        email: null,
        password: null,
      }
    }
  },
  methods: {
    submit() {
      async userLogin => {
      try {
        let response = await this.$auth.loginWith('https://travvago-backend.herokuapp.com/api/core/users/sign-in', { data: this.login })
        console.log(response)
      } catch (err) {
        console.log(err)
      }
    }
  }
}
}


//         auth: false
//       data () {
//       return {
//         auth: {
//           email: null,
//           password: null,
//         },
//       }
//     },
//     methods: {
//       submit() {
//         console.log(this.form.email),
//       }
//     }
// }
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Irish+Grover&display=swap');

.overflow-hidden{
  margin: 80px auto;
  border-radius: 5%;
  background: linear-gradient(127.44deg, rgba(108, 198, 203, 0.47) 37.36%, rgba(254, 168, 88, 0.79) 65.89%);
  
}
.image {
  filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.41));
}
.text {
  position: relative;
  color: #ffffff;
  font-size: 100px;
  text-transform: uppercase;
  font-family: 'Irish Grover', cursive;
  margin-top: -70px;
  margin-left: 150px;
  filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.41));
}
.form-group {
  margin-top: 10px;
  width: 70%;
  filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.41));
}
.title {
  margin-top: 200px;
  color:#ffffff;
  filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.41));
  
}
span {
  font-weight: bold;
  
}
.btn {
  width: 70%;
  filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.41));
}
/* tablet version */
@media (min-width: 992px) {
  .link {
    margin-right: 310px;
  }
  .button-signup {
    margin-left: 320px;
  }
}

/* Desktop Version */
@media (min-width: 992px) {
  .button-signup {
    margin-left: 225px;
  }
  .link {
    margin-right: 390px;
  }
}
</style>