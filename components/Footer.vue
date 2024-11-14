<template>
    <footer class="footer">
      <div class="footer-content">
        <div class="footer-section">
          <div class="footer-title">Link-uri utile</div>
          <a class="footer-link" @click="goToRoute('/')">Acasă</a>
          <a class="footer-link" @click="scrollToSection('products')">Produsele noastre</a>
          <a class="footer-link" @click="scrollToSection('why')">De ce Cube Furniture</a>
          <a class="footer-link" @click="scrollToSection('contact')">Contact</a>
        </div>

        <div class="footer-section">
          <div class="footer-title">Contactați-ne</div>
          <div class="contact-info">
            <Icon name="material-symbols:call-sharp" size="1.1rem" class="contact-icon" />
            <a href="tel:+40746007600" class="footer-text mobile-number">+40 746 007 600</a>
          </div>
          <div class="contact-info">
            <Icon name="material-symbols-light:mail-rounded" size="1.2rem" class="contact-icon" />
            <span class="footer-text">cubemfurniture@gmail.com</span>
          </div>
          <div class="social-info">
            <a href="https://www.facebook.com/cubemfurniture" target="_blank" style="color: #3B2E21; width: auto;">
              <Icon name="ri:facebook-circle-line" size="2.5rem" class="social-icon" />
            </a>
            <a href="https://m.me/cubemfurniture" target="_blank" style="color: #3B2E21; width: auto;">
              <Icon name="basil:facebook-messenger-outline" size="2.5rem" class="social-icon" />
            </a>
            <a href="https://wa.me/+40742391212" target="_blank" style="color: #3B2E21; width: auto;">
              <Icon name="uil:whatsapp" size="2.5rem" class="social-icon" />
            </a>
          </div>
        </div>

        <div class="footer-section">
          <div style="height: auto;">
            <img src="/assets/images/stpnation-cluj.jpg" alt="StartUp Nation">
          </div>
        </div>
      </div>
      <hr class="footer-divider" />
      <div class="footer-bottom">
        © 2024 CubeFurniture - All rights reserved
      </div>
    </footer>
  </template>

<script>
export default {
  methods: {
    goToRoute(route) {
      this.$router.push(route).then(() => {
        this.scrollToTop();
      });
    },
    goToHomeSection(section) {
      this.$router.push("/").then(() => {
        this.scrollToSection(section);
      });
    },
    scrollToSection(sectionId) {
      const section = document.getElementById(sectionId);
      if (section) {
        section.scrollIntoView({ behavior: 'smooth' });
      }
    },
    scrollToTop() {
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }
  }
}
</script>
  
  <style scoped>
    @media (min-width: 1300px) {
        .footer {
            padding-left: 9rem !important;
            padding-right: 9rem !important;
        }
    }

  .footer {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 1rem 3rem;
    color: rgb(0, 0, 0);
  }
  
  .footer-content {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    width: 100%;
  }
  
  .footer-section {
    flex: 1;
    margin: 1rem;
    min-width: 200px;
  }

  .footer-section img {
    width: 100%;
  }
  
  .footer-title {
    font-size: 1.5rem;
    margin-bottom: 0.8rem;
  }
  
  .footer-link {
    display: block;
    font-size: 1.2rem;
    color: rgb(0, 0, 0);
    margin-bottom: 0.5rem;
    text-decoration: none;
    cursor: pointer;
  }
  
  .footer-link:hover {
    text-decoration: underline;
  }
  
  .footer-text {
    font-size: 1.2rem;
  }

  .mobile-number {
    color: rgb(0, 0, 0);
    text-decoration: none;
  }
  
  .contact-info {
    display: flex;
    align-items: center;
    margin-bottom: 0.5rem;
  }

  .social-info {
    display: flex;
    align-items: center;
    gap: 1rem;
    margin-top: 2rem;
  }

  .social-icon {
    cursor: pointer;
  }
  
  .contact-icon {
    margin-right: 0.5rem;
  }
  
  .footer-divider {
    border: none;
    height: 1px;
    background-color: rgb(0, 0, 0);
    width: 100%;
    margin: 1rem 0;
  }
  
  .footer-bottom {
    text-align: center;
  }
    
  @media (max-width: 768px) {
    .footer {
        padding: 1rem 1.5rem;
    }

    .footer-content {
      flex-direction: column;
    }
    
    .footer-section {
      margin: 0.5rem 0;
      width: 100%;
    }

    .footer-section {
      margin: 0.5rem 0;
    }

    .simple-text {
        font-size: 1.2rem;
    }
  }
  </style>
  