<template>
  <div class="navbar-component">
    <div class="nav-content">
      <div class="logo">
        <i class="bx bxs-basketball"></i>
      </div>
      <ul class="nav-items">
        <li>
          <router-link class="nav-link menu-active" to="/">Home</router-link>
        </li>
        <li><router-link class="nav-link" to="/about">About</router-link></li>
        <li><router-link class="nav-link" to="/">Services</router-link></li>
        <li><router-link class="nav-link" to="/">Contact</router-link></li>
      </ul>
      <div class="login-button" @click="$router.push('/login')">Login</div>
      <div class="burger" v-on:click="isOpen = !isOpen">
        <svg
          v-show="!isOpen"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 20 20"
        >
          <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
        </svg>
        <svg
          v-show="isOpen"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 20 20"
        >
          <path
            d="M10 8.586L2.929 1.515 1.515 2.929 8.586 10l-7.071 7.071 1.414 1.414L10 11.414l7.071 7.071 1.414-1.414L11.414 10l7.071-7.071-1.414-1.414L10 8.586z"
          />
        </svg>
      </div>
    </div>

    <div class="sidenav" v-bind:class="{ 'sidenavIsOpen-sidenav': isOpen }">
      <ul class="sidenav-items">
        <li><router-link class="sidenav-link" to="/">Home</router-link></li>
        <li>
          <router-link class="sidenav-link" to="/about">About</router-link>
        </li>
        <li><router-link class="sidenav-link" to="/">Services</router-link></li>
        <li><router-link class="sidenav-link" to="/">Contact</router-link></li>
      </ul>
      <div class="sidenav-login-button" @click="$router.push('/login')">
        Login
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NavbarComponent',
  data() {
    return {
      isOpen: false,
    };
  },
  methods: {
    showMenu() {
      this.showMobileMenu = !this.showMobileMenu;
    },
  },
};
</script>

<style scoped>
.navbar-component {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  height: 70px;
  width: 100%;
  background-color: #fff;
  box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.2);
}
.hamburger_icon {
  display: none;
}
.logo i {
  color: #f85e09;
  font-size: 2rem;
}
.nav-content {
  position: relative;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 30px;
}
.nav-items {
  display: flex;
  justify-content: center;
  align-content: center;
  list-style: none;
  margin: 0;
  padding: 0;
}
li {
  padding: 0 10px;
}
.nav-link {
  font-size: 1.1rem;
  font-weight: 500;
  text-decoration: none;
}
.nav-link:hover {
  color: #f85e09;
}
.menu-active {
  color: #f85e09;
}
.login-button {
  font-size: 1.1rem;
  font-weight: 500;
  background: #fff;
  border: 1px solid #333;
  border-radius: 5px;
  padding: 10px 30px;
  cursor: pointer;
  transition: 0.4s;
}
.login-button:hover {
  color: #fff;
  background: #333;
}
.sidenav-login-button {
  font-size: 1.1rem;
  font-weight: 500;
  color: #fff;
  text-align: center;
  background: #333;
  margin: 10px 30px;
  padding: 10px 30px;
  border-radius: 5px;
  cursor: pointer;
  transition: 0.3s;
  cursor: pointer;
}
.burger {
  display: none;
  cursor: pointer;
}

.burger svg {
  fill: #333;
  height: 21px;
}

.sidenav {
  display: none;
  height: calc(100vh - 70px);
  background-color: #f85e09;
  width: 250px;
  margin-right: -250px;
  position: fixed;
  top: 70px;
  right: 0;
  transition: 0.4s;
}

.sidenav ul li {
  padding: 10px;
}
.sidenavIsOpen-sidenav {
  margin-right: 0;
  transition: 0.4s;
}

.sidenavIsOpen-main {
  opacity: 0.2;
  transition: 0.4s;
}
@media only screen and (max-width: 550px) {
  .burger {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .nav-items,
  .login-button {
    display: none;
  }
  .sidenav {
    display: block;
  }
  .sidenav-items {
    display: flex;
    flex-direction: column;
    align-items: center;
    list-style: none;
    margin: 30px;
  }
  .sidenav-link {
    font-size: 1.1rem;
    font-weight: 500;
    text-decoration: none;
    color: #fff;
  }
  .sidenav-link:hover {
    border-bottom: 2px solid #fff;
    transition: 0.4s;
  }
}
</style>
