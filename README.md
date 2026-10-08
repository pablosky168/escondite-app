# Escondite App

Aplicación web de juego de escondite con geolocalización, salas PeerJS y mapa Leaflet. Esta versión está preparada para convertirse en APK Android con Capacitor.

## Requisitos

- Node.js 18+
- Android Studio para compilar APK
- Git

## Instalar dependencias

```bash
npm install
```

## Ejecutar la web localmente

```bash
npm start
```

Abre la URL que indique la consola, normalmente:

```text
http://localhost:3000
```

## Preparar Android con Capacitor

```bash
npx cap init Escondite com.escondite.app
npx cap add android
```

## Abrir en Android Studio

```bash
npx cap open android
```

## Generar APK de depuración

```bash
npx cap sync android
cd android
./gradlew assembleDebug
```

La APK se generará en:

```text
android/app/build/outputs/apk/debug/app-debug.apk
```

## Permisos Android

En `android/app/src/main/AndroidManifest.xml`, asegúrate de incluir:

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
```

## Nota

El proyecto web está en la raíz y se sirve como página estática. La parte móvil se compila con Capacitor sin cambiar la lógica del juego.
