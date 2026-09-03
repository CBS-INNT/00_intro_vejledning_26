# Vejledning til opsætning til øvelser af innovation og ny teknologi 2026

**I denne vejledning skal slutproduktet være**
- At have Visual Studio Code eller andet IDE kørende
- At have expo, React Native frameworket kørende
- At have en github konto og have lavet dit første commit til et repository

**I mappen ovenover er opsætningen til hhv windows og mac!**

---

## Kommandoen du skal bruge hver gang

Når du opretter et nyt projekt i dette kursus, skal du altid bruge denne kommando. Kopier hele linjen:

```
npx create-expo-app@latest min_app --template blank --no-agents-md
```

Skift `min_app` ud med navnet på din app. Brug ikke æ, ø, å eller mellemrum i navnet.

`--template blank` er ikke valgfrit. Den giver dig et projekt med en `App.js`-fil, og det er den fil, alle øvelserne tager udgangspunkt i. Vælger du en anden skabelon, får du i stedet en `src/app`-mappe, og så passer vejledningerne ikke.

`@latest` sørger for, at du får den nyeste version. Den skal passe med den Expo Go-app, du henter i App Store eller Google Play.

Derefter:

```
cd min_app && npm install
```

Og start appen:

```
npx expo start
```

---

# Tips hvis du har problemer i terminalen

**Hvis Expo er langsom, eller QR-koden ikke virker på CBS-nettet:**
```
npx expo start --tunnel
```

**Hvis der er error i terminalen, så prøv:**
```
npx expo install --fix
```

**Hvis terminalen hænger, eller appen ikke opdaterer sig:**
```
npx expo start --clear
```

**Hvis du mangler navigation (bruges fra øvelse 2):**
```
npx expo install @react-navigation/native @react-navigation/native-stack @react-navigation/bottom-tabs react-native-screens react-native-safe-area-context react-native-gesture-handler react-native-reanimated react-native-get-random-values
```
