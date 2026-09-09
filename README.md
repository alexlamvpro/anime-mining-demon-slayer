# Anime Mining — Demon Slayer Edition

Telegram Mini App de minería temática **Demon Slayer**.

## Características
- Minería con sistema de energía
- Respiraciones (upgrades de tasa de minado)
- VIP 15 días (+50% minería + recompensas altas)
- 15 tareas diarias (5 con AdsGram + 10 externas)
- Sistema de referidos
- Conexión de billetera TON + retiros

## Configuración obligatoria

Abre el archivo `index.html` y busca estas líneas cerca del inicio del script principal:

```js
const ADSGRAM_BLOCK_ID = "YOUR_ADSGRAM_BLOCK_ID";
const TON_MERCHANT_ADDRESS = "EQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAM9c";
const TONCONNECT_MANIFEST_URL = "https://ton-connect.github.io/demo-dapp-with-react-ui/tonconnect-manifest.json";
```

### 1. AdsGram
1. Regístrate en [partner.adsgram.ai](https://partner.adsgram.ai)
2. Crea un bloque de tipo **Rewarded**
3. Copia el `blockId` y pégalo en `ADSGRAM_BLOCK_ID`

### 2. Wallet TON (pagos)
Pon la dirección de **tu** wallet que recibirá los pagos (formato `EQ...` o `UQ...`) en `TON_MERCHANT_ADDRESS`.

### 3. TON Connect Manifest
Crea un archivo `tonconnect-manifest.json` en tu dominio con este contenido (ajusta las URLs):

```json
{
  "url": "https://tu-dominio.com",
  "name": "Anime Mining",
  "iconUrl": "https://tu-dominio.com/icon.png",
  "termsOfUseUrl": "https://tu-dominio.com/terms",
  "privacyPolicyUrl": "https://tu-dominio.com/privacy"
}
```

Luego cambia `TONCONNECT_MANIFEST_URL` por la URL de ese archivo.

## Cómo desplegar
1. Sube `index.html` a GitHub Pages, Vercel, Netlify o cualquier hosting estático.
2. En tu Bot de Telegram (BotFather) configura el **Menu Button** o **Web App** con la URL del `index.html`.
3. Reemplaza los 3 valores de configuración anteriores.

## Repositorio
https://github.com/alexlamvpro/anime-mining-demon-slayer
