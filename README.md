# SPOT – Fishing Log App

**Autor:** Bruno  
**Studijní obor:** Aplikovaná informatika

---

## ✨ Anotace
SPOT je Android aplikace pro správu rybářských míst. Umožňuje ukládat lokality, sledovat aktuální počasí, navigovat se na uloženou lokaci a zaznamenávat informace o lovu. Aplikace je vyvinuta v Jetpack Compose a využívá OpenWeather API.

---

## 📄 Úvod
Mobilní aplikace SPOT vznikla jako pomůcka pro rybáře, kteří chtějí efektivně spravovat a uchovávat informace o svých obıíbených lovištích. Rybáři si často zapisují, kde se jim dařilo, jaké bylo počasí, jakou návnadu použili nebo jaká byla hloubka. SPOT digitalizuje tento proces.

Základní funkce aplikace zahrnují uložení pozice pomocí mapy, formulář s podrobnými informacemi, možnost prohlížení a mazání dat a navigace na danou lokalitu pomocí Google Maps. SPOT také zobrazí aktuální počasí díky OpenWeather API.  

Projekt je navržen s důrazem na jednoduchost, lokální ukládání dat bez nutnosti registrace a intuitivní ovládání i pro technický laiky.

---

## 📈 Ekonomická rozvaha

### Konkurence
Na trhu existují aplikace jako Fishbrain, Fishing Points nebo Anglr. Tyto aplikace ale často vyžadují registraci, placený obsah, a jsou složitější na ovládání.

### Výhody SPOTu
- Jednoduchost a rychlost použití
- Ukládání do zařízení (DataStore) bez cloudu
- Okamžité zobrazení počasí
- Možnost integrace navigace

### Propagace
- Osobní značka a propagace na sociálních sítích a rybářských skupinách
- Plakáty a QR kódy na rybářských událostech

### Investice a návratnost
Aplikace byla vyvinuta zdarma ve volném čase. Možné monetizační modely:
- Reklamy (AdMob)
- Jednorázové odemčení premium funkcí

---

## 🛠️ Vývoj

### Použité technologie
- **Jetpack Compose**: UI framework
- **Navigation Compose**: navigace mezi obrazovkami
- **Retrofit + Gson**: HTTP klient pro OpenWeather API
- **DataStore**: ukladání dat do interní paměti
- **Coil**: Načítání ikony počasí

### Struktura projektu
```
com.example.spot
|-- data
|   |-- DataStoreManager.kt
|   |-- FishingSpot.kt
|-- network
|   |-- RetrofitInstance.kt
|   |-- WeatherApiService.kt
|-- screens
|   |-- MapScreen.kt
|   |-- AddSpotScreen.kt
|   |-- SavedPlacesScreen.kt
|   |-- CatchRecordsScreen.kt
|-- navigation
|   |-- NavGraph.kt
|-- MainActivity.kt
```

### Průběěh vývoje
- Fáze 1: Základní funkčnost (mapa, formulář, uložení)
- Fáze 2: Počasí a navigace
- Fáze 3: Vzhled a testování


---

## ✅ Testování

| Scénář | Popis | Očekávaný výsledek | Stav |
|--------|--------|-------------------------|------|
| 1 | Uložení místa na mapě | Místo se uloží s detailními informacemi | ✅ |
| 2 | Zobrazení uložených míst | Seznam zobrazuje data včetně počasí | ✅ |
| 3 | Navigace z detailu | Google Maps se otevře s trasou | ✅ |
| 4 | Smazání místa | Místo zmizí ze seznamu | ✅ |
| 5 | Spuštění na emulátoru | Aplikace se otevře bez pádu | ✅ |


---

## 🌐 Nasazení a spuštění
###Projek je pořád ve fázi vývoje a zatím je pouze pro nejblžší okruh přátel
###Zde je způsob jak projekt spustit, než se vydá verze pro veřejnost:
### Požadavky:
- Android Studio Flamingo+
- Zařízení nebo emulátor s Google Maps

### Kroky:
1. Zaregistruj se na https://openweathermap.org a získej API klíč
2. Vlož ho do `RetrofitInstance.kt`
3. Povol oprávnění v `AndroidManifest.xml`:
```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
```
4. Spusť projekt v Android Studiu (Run)




---

## ✏️ Závěr
Tento projekt vznikl jako kombinace osobního koníčku a vývojářské zkušenosti.  
SPOT výrazně zjednodušuje správu rybářských míst. I když je stále ve vývoji, již nyní je plně funkční a použitelný v terénu.  

Cílem je v budoucnu přidat přihlášení, synchronizaci s cloudem a více statistik pro lov.  
Děkuji všem, kdo projekt testovali a poskytli zpětnou vazbu.

---

