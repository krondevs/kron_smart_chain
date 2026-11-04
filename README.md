# Kron Smart Chain (KSC)

> **Contratos inteligentes de nivel EVM integrados con la seguridad inmutable y el modelo UTXO de Bitcoin.**

**Kron Smart Chain (KSC)** es una plataforma blockchain de alto rendimiento basada en la arquitectura híbrida de Qtum Core. Combina lo mejor de dos mundos: la **seguridad inquebrantable y eficiencia de recursos del modelo UTXO** junto con la **flexibilidad programable de la Ethereum Virtual Machine (EVM)**. 

KSC opera como una red independiente de capa 1 con su propio bloque génesis, parámetros de red optimizados, economía de Staking sostenible (PoS) y un ecosistema listo para aplicaciones descentralizadas de alto volumen.

---

## 🚀 ¿Qué problemas resuelve Kron Smart Chain?

### 1. Cuellos de botella y costos de gas impredecibles en Ethereum
* **Problema:** En redes tradicionales basadas en cuentas como Ethereum, las comisiones de gas se disparan durante periodos de congestión, haciendo inviables los micropagos y las llamadas continuas a contratos.
* **Solución KSC:** Gracias al modelo UTXO y al algoritmo Proof of Stake (PoS), las transacciones son altamente predecibles y eficientes. Las comisiones se mantienen fraccionarias, permitiendo microtransacciones comerciales sin afectar la rentabilidad.

### 2. Falta de verificación estricta en modelos de cuenta tradicionales
* **Problema:** El modelo tradicional de cuentas procesa transacciones en serie y puede sufrir vulnerabilidades de estado global si un contrato inteligente presenta fallas de reentrancia o ejecución incompleta.
* **Solución KSC:** El motor **Account Abstraction Layer (AAL)** conecta la EVM con el modelo UTXO de Bitcoin. Esto permite que las transacciones y estados de los contratos inteligentes sean seguros, paralelizables en verificación y auditables de forma determinista.

### 3. Consumo masivo de energía y barreras de entrada para validadores
* **Problema:** La minería PoW exige hardware sumamente costoso y alto consumo eléctrico, mientras que muchas redes PoS imponen montos mínimos prohibitivos para operar un nodo.
* **Solución KSC:** Cualquier usuario o nodo puede participar en el consenso y asegurar la red mediante **Offline Staking** o validación local con un consumo de energía insignificante, garantizando la descentralización efectiva de la red.

---

## 💡 Casos de Uso en la Vida Real

* **🔐 Sistemas de Licenciamiento ERP y Software Empresarial:** Emisión de licencias digitales vinculadas criptográficamente al hardware del cliente (HWID hashes), gestionando validez temporal (DEMO, ANUAL, LIFETIME) mediante contratos inteligentes sin depender de servidores centrales de activación.
* **📦 Trazabilidad en Cadenas de Suministro:** Integración nativa con sistemas ERP para registrar eventos de producción, números de lote y certificados de calidad directamente en la blockchain mediante tokens ERC-20 o ERC-721.
* **🎓 Titulación y Certificación Inmutable:** Emisión e inspección instantánea de títulos universitarios, diplomas y certificados de autenticidad a costo mínimo, garantizando protección contra falsificaciones y verificación pública inmediata.
* **💳 Pasarelas de Pago y Microtransacciones dApp:** Ejecución de micropagos automatizados para e-commerce, plataformas de contenido y videojuegos donde la velocidad de confirmación y las bajas comisiones son requisitos fundamentales.

---

## 🛠️ Suite de Binarios

| Binario | Función y Descripción |
|---|---|
| `krond` | Daemon principal del nodo completo y motor de validación. |
| `kron-cli` | Cliente de línea de comandos para interacción RPC y gestión de nodo. |
| `kron-qt` | Billetera de interfaz gráfica (GUI) nativa basada en Qt6. |
| `kron-tx` | Herramienta CLI para creación y firma de transacciones offline. |
| `kron-util` | Suite de utilidades criptográficas e inspección de bloques. |
| `kron-wallet` | Herramienta técnica para gestión y recuperación de billeteras. |

*Los binarios compilados se generan en la carpeta `build/bin/`.*

---

## 🌐 Parámetros de Red

### Mainnet (Red Principal)

| Parámetro | Valor |
|---|---|
| **Chain ID EVM** | `2026` |
| **Puerto P2P** | `20888` |
| **Puerto RPC** | `20889` |
| **Puerto Tor (.onion)** | `20891` |
| **Magic Message** | `KRON` (`4b 52 4f 4e`) |
| **Prefijo P2PKH** | `45` (Direcciones `K...`) |
| **Prefijo P2SH** | `63` (Direcciones `S...`) |
| **Bech32 HRP** | `kron` (Direcciones `kron1...`) |
| **WIF Prefix** | `128` |
| **Génesis Hash** | `00003cc638750628bca7fac735888a303e7c87cf198f5611af57e48f0b4f1688` |
| **Merkle Root Génesis** | `ce401e2ab0b9c6ed4f7441a9d97429b82d7800305bcde19fcb557105e42d736b` |
| **Timestamp Génesis** | `1793664000` (2026-11-03 00:00:00 UTC) |

### Entornos de Desarrollo y Pruebas

| Red | Puerto P2P | Puerto RPC | Magic | HRP Bech32 |
|---|---:|---:|---|---|
| **Testnet3** | `21888` | `21889` | `KRT3` | `tkron` |
| **Testnet4** | `22888` | `22889` | `KRT4` | `t4kron` |
| **Signet** | `23888` | `23889` | `KRSG` | `skron` |
| **Regtest** | `24888` | `24889` | `KRRT` | `qcrt` |

---

## 📂 Directorios de Trabajo

- **Directorio de datos predeterminado:** `~/.kron`
- **Archivo de configuración principal:** `~/.kron/kron.conf`
- **Almacenamiento de billeteras:** `~/.kron/wallets/`

---

## 📄 Licencia y Créditos
Este proyecto se distribuye bajo la licencia MIT.

Créditos: Kron Smart Chain se desarrolla a partir de la arquitectura base de Qtum Core y Bitcoin Core, conservando las licencias y derechos de autor originales e integrando su propia identidad de red, génesis, puertos, parámetros EVM y marca.

⚠️ Aviso de Responsabilidad: Kron Smart Chain es software criptográfico experimental. Realice las auditorías de seguridad y pruebas necesarias en entornos Regtest o Testnet antes de su uso en produccion
