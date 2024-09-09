<template>
  <nav class="navbar">
    <!-- Logo Section -->
    <div class="navbar-logo">
      <span> Logo </span>
    </div>

    <!-- Hamburger Menu Icon (Mobile View) -->
    <div class="hamburger" @click="toggleMenu">
      <div :class="{ 'is-active': menuOpen }" class="hamburger-lines"></div>
    </div>

    <!-- Menu Section -->
    <div :class="['navbar-menu', { 'menu-open': menuOpen }]">
      <ul class="menu-items">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
      <button class="signup-button">Sign Up</button>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      menuOpen: false, // Controls whether the menu is open or closed
    };
  },
  methods: {
    toggleMenu() {
      this.menuOpen = !this.menuOpen;
    },
  },
};
</script>

<style scoped>
/* Navbar Container */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 30px;
  background-color: #f8f9fa;
  border-bottom: 1px solid #eaeaea;
  position: relative;
}

/* Logo Section */
.navbar-logo .logo {
  height: 50px;
}

/* Menu Section (Desktop View) */
.navbar-menu {
  display: flex;
  align-items: center;
}

.menu-items {
  display: flex;
  list-style: none;
  margin: 0;
  padding: 0;
}

.menu-items li {
  margin: 0 15px;
}

.menu-items li a {
  text-decoration: none;
  color: #333;
  font-weight: 500;
  font-size: 16px;
}

.signup-button {
  background-color: #007bff;
  color: white;
  border: none;
  padding: 8px 16px;
  border-radius: 4px;
  cursor: pointer;
  font-size: 16px;
  margin-left: 20px;
  transition: background-color 0.3s;
}

.signup-button:hover {
  background-color: #0056b3;
}

/* Hamburger Icon (Mobile View) */
.hamburger {
  display: none;
  cursor: pointer;
}

.hamburger-lines {
  width: 30px;
  height: 3px;
  background-color: #333;
  position: relative;
  transition: all 0.3s ease-in-out;
}

.hamburger-lines::before,
.hamburger-lines::after {
  content: "";
  width: 30px;
  height: 3px;
  background-color: #333;
  position: absolute;
  left: 0;
  transition: all 0.3s ease-in-out;
}

.hamburger-lines::before {
  top: -8px;
}

.hamburger-lines::after {
  top: 8px;
}

/* When the Hamburger Menu is Active (Transforms into an "X") */
.is-active {
  background-color: transparent;
}

.is-active::before {
  transform: rotate(45deg);
  top: 0;
}

.is-active::after {
  transform: rotate(-45deg);
  top: 0;
}

/* Responsive Styling for Mobile */
@media (max-width: 768px) {
  .navbar-menu {
    display: none;
    flex-direction: column;
    position: absolute;
    top: 60px;
    right: 0;
    background-color: white;
    width: 100%;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }

  .menu-open {
    display: flex;
  }

  .menu-items {
    flex-direction: column;
    align-items: center;
  }

  .menu-items li {
    margin: 10px 0;
  }

  .signup-button {
    margin: 15px 0;
  }

  .hamburger {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 30px;
    height: 30px;
  }
}

@media (max-width: 480px) {
  .navbar-logo .logo {
    height: 40px;
  }
}
</style>
