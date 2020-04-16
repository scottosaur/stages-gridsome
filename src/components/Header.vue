<template>
  <div>
    <header class="header">
      <g-link class="header__logo" to="/">
        <!-- {{ $static.metadata.siteName }} -->
        <!-- img tag used instead of g-image per suggestion from developer: https://github.com/gridsome/gridsome/issues/189  -->
        <img
          src="../assets/images/stages-logo-svg.svg"
          alt="Stages Performing Arts"
        />
      </g-link>

      <nav class="primary-nav">
        <ul>
          <li id="classes-link" class="primary-nav__drop-link">
            <a href="index.html#classes" title="Classes">Classes</a>
            <i class="fas fa-angle-down"></i>
            <ul class="primary-nav__drop-menu">
              <li>
                <a
                  href="classes-infant-toddler.html"
                  title="Newborn to 18 Months"
                  >Newborn to 18 Months</a
                >
              </li>
              <li>
                <a
                  href="classes-preschool-prep.html"
                  title="18 Months to 3 Years"
                  >18 Months to 3 Years</a
                >
              </li>
              <li>
                <a href="classes-preschool.html" title="3 Years to 5 Years"
                  >3 Years to 5 Years</a
                >
              </li>
              <li>
                <a href="classes-grade-school.html" title="K to 6th Grade"
                  >K to 6th Grade</a
                >
              </li>
            </ul>
          </li>
          <li id="parties-and-events-link">
            <a href="parties-events.html" title="Parties & Events"
              >Parties & Events</a
            >
          </li>
          <li id="camps-link" class="primary-nav__drop-link">
            <a href="index.html#camps" title="Camps">Camps</a>
            <i class="fas fa-angle-down"></i>
            <ul class="primary-nav__drop-menu">
              <li>
                <a href="camps-mini-camp.html" title="Mini Camp">Mini Camp</a>
              </li>
              <li>
                <a href="camps-little-stars.html" title="Little Stars"
                  >Little Stars</a
                >
              </li>
            </ul>
          </li>
          <li id="about-link">
            <a href="about.html" title="About">About</a>
          </li>
          <li id="contact-link">
            <a href="#contact" title="Contact Us">Contact Us</a>
          </li>
          <li>
            <a href="register.html">
              <button class="btn btn--blue">Register Now</button>
            </a>
          </li>
        </ul>
      </nav>
    </header>
    <div class="header-spacer"></div>
  </div>
</template>

<style lang="scss">
.header {
  background-color: orange;
  position: relative;
  height: 110px;
  overflow: visible;
  display: flex;
  justify-content: space-between;
  align-items: center;
  z-index: 20;

  @include atMedium {
    align-items: flex-end;
    justify-content: space-between;
    position: fixed;
    background-color: $testGreen;
    width: 100%;
    max-width: inherit;
    margin: auto;
    z-index: 5;
    top: 0;
    height: 145px;
    transition: all 0.2s ease-out;

    &--reduced {
      height: 60px;
      background-color: rgba(255, 255, 255, 0.85);
    }
  }

  &__logo {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100%;
    padding: 0;

    img {
      max-width: 90%;
      max-height: 90%;
    }
  }

  &__menu-button {
    font-size: 2rem;
    visibility: visible;
    margin-right: 15px;

    @include atMedium {
      display: none;
    }
  }

  .primary-nav {
    display: none;

    @include atMedium {
      display: block;
    }
  }
}

.header-spacer {
  @include atMedium {
    transition: all 0.2s ease-out;
    margin-top: 145px;

    .reduced {
      margin-top: 110px;
    }
  }
}
</style>
