<template>
  <v-app class="fondo-campus" :style="{ backgroundImage: `url(${imagenFondo})` }">
    <v-container class="fill-height d-flex justify-center align-center">
      
      <v-card class="pa-8 text-center tarjeta-interfaz" max-width="450" elevation="10" rounded="lg">
        
        <v-img 
          :src="logoUnibague"
          alt="Escudo de la Universidad de Ibagué"
          max-height="120"
          contain
          class="mb-4 mx-auto"
        ></v-img>
        
        <h1 class="text-h5 font-weight-bold text-slate-900 mb-2">
          Centro de Descargas de Seguridad
        </h1>
        
        <p class="text-body-1 text-grey-darken-2 mb-6">
          Haz clic en el botón de abajo para obtener el instalador oficial de Kaspersky Antivirus para tu sistema.
        </p>

        <!-- Enlace corregido al instalador público correcto -->
        <v-btn
          href="/kaspersky_installer.exe"
          download="Instalador_Kaspersky.exe"
          size="x-large"
          class="text-white font-weight-bold px-8 custom-hover-btn"
          rounded="md"
          elevation="3"
        >
          <v-icon start class="mr-2">mdi-download</v-icon>
          Descargar Kaspersky
        </v-btn>

        <div class="text-caption text-grey-darken-1 mt-6 font-weight-medium">
          Versión: 2026
        </div>
        
      </v-card>

    </v-container>
  </v-app>
</template>

<script setup>
// Importamos ambos recursos desde la carpeta assets usando rutas relativas seguras
import logoUnibague from './assets/logo-unibague.webp'
import imagenFondo from './assets/campus.jpeg'
</script>

<style scoped>
/* Estilos para que la imagen ocupe toda la pantalla de fondo de manera perfecta */
.fondo-campus {
  background-size: cover !important;
  background-position: center center !important;
  background-repeat: no-repeat !important;
  background-attachment: fixed !important;
}

/* Estilo opcional para la tarjeta: un fondo ligeramente translúcido para que se fusione con el paisaje */
.tarjeta-interfaz {
  background-color: rgba(255, 255, 255, 0.92) !important;
  backdrop-filter: blur(4px); /* Suave efecto de desenfoque detrás de la tarjeta */
}

/* CORRECCIÓN: Añadimos tu Azul Rey base directamente aquí */
.custom-hover-btn {
  background-color: #00248f !important; /* Tu azul rey puro original */
  color: #ffffff !important;
  transition: all 0.2s ease !important;
}

/* Efecto hover personalizado del botón */
.custom-hover-btn:hover {
  background-color: #5A82F7 !important; /* Tu azul rey más claro */
  transform: translateY(-2px);
  box-shadow: 0 6px 16px rgba(65, 105, 225, 0.4) !important;
}

.custom-hover-btn:active {
  transform: translateY(0);
}
</style>