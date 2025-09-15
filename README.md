# Allarme GasBT

## Descrizione Progetto

**Allarme GasBT** è un sistema di monitoraggio per camper e ambienti mobili che rileva la presenza di gas pericolosi e consente di gestire allarmi e dispositivi tramite Bluetooth e WiFi.  
Il progetto nasce come evoluzione del sistema antintrusione per camper, integrando sensori per la qualità dell'aria e la rilevazione di gas, oltre a controlli remoti tramite app Flutter.

## Funzionalità principali

- Rilevazione gas infiammabili e nocivi (MQ2, MQ135)
- Notifica via Bluetooth/Smartphone
- Attivazione relay per dispositivi di sicurezza (sirena, ventola, ecc.)
- Gestione LED RGB per segnalazioni visive
- Visualizzazione dati su display LCD 1.14"
- Espansione con altri moduli (sensori, attuatori)
- Compatibile con app Flutter dedicata

---

## Sviluppo App

L’applicazione mobile di controllo e monitoraggio viene sviluppata con **Flutter**, utilizzando **Visual Studio Code** (VS Code) come ambiente di sviluppo principale.  
Questo consente la massima compatibilità per Android e iOS, oltre a una facile integrazione con l’hardware ESP32 tramite Bluetooth.

**Requisiti di sviluppo:**
- [Flutter SDK](https://docs.flutter.dev/get-started/install)
- [Visual Studio Code](https://code.visualstudio.com/)
- Estensione Flutter/Dart per VS Code
- Android Studio (opzionale, solo per emulatori e strumenti Android)

**Vantaggi:**
- Sviluppo multipiattaforma
- Debug rapido
- Integrazione con dispositivi hardware via Bluetooth/WiFi

---

## Hardware utilizzato

### Scheda di sviluppo:  
**diymore per ESP32**  
- Display LCD da 1,14 pollici
- Chip CH340  
- USB-C  
- WiFi 2.4 GHz  
- Bluetooth  
- Compatibile ESP32 Nodemcu

### Moduli aggiuntivi:
- **Relay**: per attivazione dispositivi esterni
- **LED RGB KY-016 (FZ0455)**: Modulo a 3 colori per segnalazioni visive
- **Sensori gas**:  
  - **MQ-2**: rilevazione gas infiammabili (metano, GPL, fumo, ecc.)
  - **MQ-135**: rilevazione qualità dell'aria e gas nocivi (ammoniaca, benzene, CO2, ecc.)

### Schema di collegamento (testuale)

- ESP32 LCD: connessioni standard GPIO
- Relay: collegato a GPIO digitale (es. D12)
- LED RGB KY-016: collegato a 3 GPIO PWM (es. D13, D14, D15)
- MQ-2: ingresso analogico (es. A0)
- MQ-135: ingresso analogico (es. A1)

---

## Esempi di utilizzo

- Rilevazione gas pericolosi e attivazione allarme.
- Invio notifica a smartphone tramite app Flutter.
- Accensione LED RGB per segnalazione visiva.
- Visualizzazione stato sensori su display LCD.

---

## Repository e struttura

All’interno di questo repository trovi anche:

### 1. **Progetto Flutter**
Cartella `/flutter_app/`:  
Contiene il codice sorgente dell'app Flutter per la gestione e il monitoraggio del sistema Allarme GasBT.  
L’app consente di:
- Ricevere dati dai sensori via Bluetooth
- Visualizzare lo stato dei sensori e dispositivi
- Gestire le notifiche di allarme
- Attivare/disattivare le funzioni di sicurezza

### 2. **Progetto INO esempio: Allarme Camper Antintrusione**
Cartella `/allarme-camper-antintrusione/`:  
Contiene uno sketch di esempio per ESP32/Arduino, dedicato all’antintrusione per camper.  
Questo progetto dimostra come collegare sensori di movimento, attivare relay e inviare notifiche di allarme tramite Bluetooth.  
Può essere usato come base per personalizzazioni e integrazioni con il sistema gas.

### 3. **Progetto principale Gas**
Cartella `/allarme_gasbt/`:  
Contiene il codice sorgente per il monitoraggio gas (ESP32), con gestione sensori MQ-2/MQ-135, relay e LED RGB.

### 4. **Documentazione**
Cartella `/docs/`:  
Guide, tutorial, schemi di collegamento, informazioni tecniche su hardware e software.

---

## Riferimenti utili

- [MQ2 datasheet](https://www.sparkfun.com/datasheets/Sensors/MQ-2.pdf)
- [MQ135 datasheet](https://www.electronicwings.com/nodemcu/mq135-gas-sensor-interfacing-with-nodemcu)
- [KY-016 info](https://www.keyestudio.com/keyestudio-ky-016-3-color-rgb-led-module-for-arduino-p0072.html)
- [ESP32 info](https://www.espressif.com/en/products/socs/esp32)
- [Flutter](https://flutter.dev)
- [Visual Studio Code](https://code.visualstudio.com/)

---

## Autore

Fabio (fabiuz73)

---

## Note

Per richieste, suggerimenti o collaborazioni, aprire una issue nel repository.