<template>
  <div id="app">
    <footer>
      <div class="component fpc-footer">
        <div class="component fpc-grid container-fluid">
          <div class="row">
            <div class="col">
              <div class="component fpc-grid container">
                <div class="row">
                  <div class="col">
                    <p class="h4">ACME Inc Pty Ltd</p>
                    <div class="fpc-footer__row-one row">
                      <div class="col-12 col-lg-4">
                        <div class="component fpc-wysiwyg">
                          <p>
                            Quisque quis diam vel mauris congue tempus. Sed
                            finibus dapibus ex, vel maximus ex feugiat a.
                            Vestibulum nec odio ex. Integer sed sodales erat, ut
                            suscipit lectus. Morbi commodo ultricies est sed
                            euismod. Nullam sollicitudin quam arcu.
                          </p>
                        </div>
                      </div>
                      <div class="col-12 col-lg-3 offset-lg-1">
                        <div class="component fpc-wysiwyg fpc-wysiwyg--white">
                          <p class="colour-fg--grey-700 mb-0">
                            <strong>For all enquiries</strong>
                          </p>
                          <p>
                            <a href="mailto:info@acmeinc.com"
                              >info@acmeinc.com</a
                            >
                          </p>
                          <p class="colour-fg--grey-700 mb-0">
                            <strong>A part of</strong>
                          </p>
                          <p>ACME Inc Pty Ltd</p>
                        </div>
                      </div>
                      <div class="col-12 col-lg-2">
                        <div class="component fpc-wysiwyg fpc-wysiwyg--white">
                          <p><a href="#">About Us</a></p>
                          <p><a href="#">What we do</a></p>
                          <p><a href="#">Who we are</a></p>
                          <p><a href="#">News</a></p>
                          <p><a href="#">Testimonials</a></p>
                        </div>
                      </div>
                      <div class="col-12 col-lg-2">
                        <div class="fpc-footer__social-links-column">
                          <div class="fpc-footer__social-links">
                            <a href="#" target="_blank" rel="noopener">
                              <img
                                src="https://www.switchit.com/hosted-images/fed-test/logo-linkedin.svg#svgView(viewBox(0,0,31,31))"
                                alt="LinkedIn"
                              />
                            </a>
                            <a href="#" target="_blank" rel="noopener">
                              <img
                                src="https://www.switchit.com/hosted-images/fed-test/logo-youtube.svg#svgView(viewBox(0,0,40,40))"
                                alt="YouTube"
                              />
                            </a>
                            <a href="#" target="_blank" rel="noopener">
                              <img
                                src="https://www.switchit.com/hosted-images/fed-test/logo-twitter.svg#svgView(viewBox(0,0,40,40))"
                                alt="Twitter"
                              />
                            </a>
                          </div>
                          <p class="fpc-footer__copyright">
                            &copy; ACME Inc Pty Ltd
                          </p>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
</script>

<style lang="scss">
@import url('https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/css/bootstrap.min.css');

// Test 1: IE11 Styling
// footer looks OK in modern browsers, however there is a layout issue when viewed in IE11. troubleshoot the problem
// use the "Debug View" to see the page in IE

/*! variables */
$grid-gutter-width: 40px;
$grid-gutter-width-half: $grid-gutter-width / 2;

$spacer: 16px;
@function gutter-size($gutter-multiplier) {
  @return $spacer * $gutter-multiplier;
}

$white: #fff;
$gray-100: #fafafa;
$gray-200: #f5f5f5;
$gray-300: #e6e7e8;
$gray-400: #dbd5cd;
$gray-500: #d5d5d5;
$gray-600: #a7a9ab;
$gray-700: #808284;
$gray-800: #585858;
$gray-900: #292929;
$black: #000;

// brand
$primary: #ed1c24;
$secondary: #80000b;

// font sizes
$font-size-base: 1rem;
$font-size-base-px: 16px;
$font-size-sm: $font-size-base * 0.875;

$opacity-base: 1;
$opacity-half: $opacity-base * 0.5;

// link states
$interact: '&:focus, &:hover, &:active';

/*! base */
body {
  color: $white;
}

/*! footer */
.fpc-footer {
  padding: gutter-size(3) 0 0 0;
  background-color: #313131;

  // first row
  &__row-one {
    padding-bottom: gutter-size(3.125);
    > .col-12 {
      &:nth-child(1) {
        .h4 {
          margin-top: 0;
        }
      }
      &:nth-child(2),
      &:nth-child(3),
      &:nth-child(4) {
        border-left: 1px solid rgba($gray-600, 0.5);
        > div {
          a {
            text-decoration: none;
          }
        }
      }
      &:nth-child(2) {
        a {
          color: $white;
          text-decoration: none;
          word-break: break-all;
          #{$interact} {
            opacity: $opacity-half;
          }
        }
      }
      &:nth-child(3) {
        .h7 {
          margin: 0;
          color: $gray-600;
        }
        p {
          margin: 0 0 gutter-size(0.75) 0;
          &:last-child {
            margin-bottom: 0;
          }
        }
        a {
          color: $gray-600;
          #{$interact} {
            color: $white;
          }
        }
      }
    }
  }
  &__social-links {
    a {
      position: relative;
      display: inline-block;
      margin: 0 gutter-size(0.75) gutter-size(1) 0;
      vertical-align: bottom;
      &:last-child {
        margin-right: 0;
      }
      &:focus,
      &:hover {
        &:before {
          box-shadow: inset 0 0 0 1px $gray-900;
        }
      }
      &:before {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: $primary;
        border-radius: 100%;
        box-shadow: inset 0 0 0 gutter-size(2) #313131;
        transition: box-shadow 0.25s ease;
        content: '';
      }
      img {
        position: relative;
        display: inline-block;
        width: gutter-size(2.5);
        height: gutter-size(2.5);
        vertical-align: bottom;
      }
    }
  }

  &__social-links-column {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 100%;
  }

  &__copyright {
    font-size: $font-size-sm;
  }

  @media (max-width: 991.98px) {
    // row one
    &__row-one {
      margin-top: gutter-size(-1.5);
      > .col-12 {
        &:nth-child(2),
        &:nth-child(3),
        &:nth-child(4) {
          border-left: none;
          > div {
            border-left: none;
          }
        }
        &:nth-child(1) {
          > div {
            padding: gutter-size(2) 0;
          }
        }
        &:nth-child(2) {
          > div {
            padding: gutter-size(1) 0;
          }
        }
        &:nth-child(3) {
          > div {
            margin: gutter-size(1) 0 0 0;
            padding: gutter-size(1.5) 0;
            border-top: 1px solid $gray-800;
            border-bottom: 1px solid $gray-800;
          }
        }
        &:nth-child(4) {
          > div {
            padding: gutter-size(2.5) 0;
          }
        }
      }
    }
  }
  @media (min-width: 992px) {
    padding: gutter-size(5) 0 0 0;
    &__social-links {
      a {
        margin-right: gutter-size(0.5);
      }
    }
  }
}


</style>
