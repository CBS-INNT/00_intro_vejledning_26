# Opsætning af expo - React native Mobil apps (Mac)

1. Start med at åbne din terminal i VS Code

2. **Hvis du får adgangsproblemer med at køre kommandoer i denne guide, skriv `sudo` før hvert kommando for at køre det som administrator**

3. Hvis du oplever fejl med kommandoer, læs først hvad terminalen siger og prøv selv at rette det, hvis det ikke lykkes, tilkald hjælp

## Node

1. Tjek om det er installeret ved at skrive følgende:

```
node -v
```

2. Hvis den giver et versionsnummer som `v20.19.4` eller højere, så er du good to go. Hop videre til Expo.

3. Hvis du får `zsh: command not found`, eller et lavere versionsnummer, skal du hente Node.

### Download Node

Følg den officielle hjemmeside og hent **LTS-versionen**: https://nodejs.org/en

Tjek bagefter at det virkede:

```
node -v && npm -v
```

## Expo

1. Gå til https://expo.dev/ og lav en konto ved at trykke på "Sign Up"

2. Download Expo Go på din mobil fra App Store eller Google Play

### Start dit første expo projekt!

Vi anbefaler, at I laver en mappe "INNT_Exercises", hvor I kan gemme jeres opgaver.

1. Åbn Visual Studio Code (VS Code), åbn jeres mappe, og åbn en terminal i VS Code.

2. Kør denne kommando. **Kopier hele linjen** — alle dele af den betyder noget:

```
npx create-expo-app@latest min_app --template blank --no-agents-md
```

3. Når den er færdig, gå ind i projektet og installer pakkerne:

```
cd min_app && npm install
```

4. Start appen:

```
npx expo start
```

5. Scan QR koden på skærmen og se appen på din telefon! 😲

6. Du skulle nu se teksten `Open up App.js to start working on your app!`

7. Prøv at ændre teksten i `App.js` og se den ændre sig på telefonen

---

# Tips hvis du har problemer i terminalen

**Hvis QR-koden ikke virker på CBS-nettet / eduroam**

Stop appen med `Ctrl + C` og start den med tunnel i stedet:

```
npx expo start --tunnel
```

Virker det stadig ikke, så del mobilhotspot fra din telefon til din computer.

**Hvis der er error i terminalen efter du har installeret pakker**

```
npx expo install --fix
```

**Hvis terminalen hænger, eller appen ikke opdaterer sig**

Stop med `Ctrl + C` og start forfra med tom cache:

```
npx expo start --clear
```

**Hvis du senere skal bruge navigation (fra øvelse 2)**

```
npx expo install @react-navigation/native @react-navigation/native-stack @react-navigation/bottom-tabs react-native-screens react-native-safe-area-context react-native-gesture-handler react-native-reanimated react-native-get-random-values
```
