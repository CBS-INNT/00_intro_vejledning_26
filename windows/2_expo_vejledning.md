# Opsætning af expo Windows - React native Mobil apps

#### En forudsætning for at kunne installere expo er at man har hentet node

- Du kan tjekke om du allerede har node ved at skrive følgende i terminalen:

```
node -v
```

- Hvis terminalen returnerer `v20.19.4` eller højere, er alt i orden og du kan hoppe til næste punkt i denne vejledning.

- Ellers: hent den anbefalede version (**LTS**) af Node her: https://nodejs.org/en

- Tjek bagefter at det virkede:

```
node -v && npm -v
```

#### Installer Expo Go

- Hent Expo Go appen på din telefon fra Google Play eller App Store: https://docs.expo.dev/get-started/set-up-your-environment/

- Lav også en konto på https://expo.dev/

#### Kør dit første expo projekt!

1. Navigér i terminalen ind til den mappe, som projektet skal placeres i (`cd` & `cd..`)

2. Kør denne kommando. **Kopier hele linjen** — alle dele af den betyder noget:

```
npx create-expo-app@latest min_app --template blank@sdk-54
```

3. Gå ind i projektet og installer pakkerne:

```
cd min_app && npm install
```

4. Åbn projektet i VS Code og aktivér det ved at skrive i terminalen:

```
npx expo start
```

5. Dernæst åbnes terminalen med expo interfacet. Check først at din computer og telefon kører på det samme net. Scanning af QR-koden foregår ved brug af Expo Go appen.

6. Resultatet skulle være at du ser denne tekst: `Open up App.js to start working on your app!`

7. Prøv at ændre i filen `App.js` og se teksten ændre sig

---

# Tips hvis du har problemer i terminalen

**OBS! Hvis cbs-nettet / eduroam ikke virker**

Stop appen med `Ctrl + C` og start den med tunnel i stedet:

```
npx expo start --tunnel
```

Virker det stadig ikke, kan det være nødvendigt at gå på mobil-hotspot.

**Hvis du får "Project is incompatible with this version of Expo Go"**

Så er dit projekt lavet med en for ny version. Slet mappen og lav den igen:

```
cd .. && rmdir /s /q min_app && npx create-expo-app@latest min_app --template blank@sdk-54 && cd min_app && npm install
```

Husk `--template blank@sdk-54` — uden den kan appen ikke åbnes på iPhone.

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
