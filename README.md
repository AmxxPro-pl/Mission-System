<div align="center">
  <h1>Missions Professional System</h1>
  <img src="https://github.com/AmxxPro-pl/.github/blob/main/banner-new-2.png" alt="Missions Pro Banner" width="100%">
</div>

---

### 📝 Opis / Description
**PL:** **Missions Pro** to najbardziej wydajny i modułowy silnik misji dla serwerów Counter-Strike 1.6. System pozwala na tworzenie nielimitowanej liczby zadań podzielonych na akty. Dzięki unikalnej architekturze opartej na sub-pluginach, system idealnie współpracuje z trybami takimi jak **JailBreak** oraz **CoD Mod**, oferując dedykowane typy misji przy zachowaniu maksymalnej optymalizacji.

**EN:** **Missions Pro** is the most efficient and modular mission engine for Counter-Strike 1.6. It allows creating unlimited tasks divided into acts. Thanks to the sub-plugin architecture, the system works perfectly with modes like **JailBreak** and **CoD Mod**, offering dedicated mission types while maintaining maximum performance.

---

### ✨ Główne Cechy / Key Features
* ⚙️ **Modular Architecture** - Osobne moduły dla JB, CoD Mod i misji ogólnych (Core).
* 📚 **Act System** - Możliwość dzielenia misji na rozdziały (Akty) dla lepszej progresji.
* 💾 **MySQL Database** - Stabilny i bezpieczny zapis postępów gracza w chmurze.
* 💰 **Rewards System** - Automatyczne przyznawanie waluty (Szlugi, Monety, $) lub nagród specjalnych.
* 🛠️ **Developer API** - Bogaty zestaw natywów i forwardów dla twórców dodatków.
* 📊 **Modern UI** - Nowoczesne menu szczegółów misji spójne wizualnie z systemem skinów.

---

### 📸 ScreenShots

#### 🎮 Powiadomienia i Status (HUD)
| Status Misji (StatusText) | Status Misji (StatusText) | Postęp Misji (DHUD) |
|:---:|:---:|:---:|
| <img src="https://github.com/AmxxPro-pl/Mission-System/blob/main/assets/Screenshot_1.png" width="400"> | <img src="https://github.com/AmxxPro-pl/Mission-System/blob/main/assets/Screenshot_5.png" width="400"> | <img src="https://github.com/AmxxPro-pl/Mission-System/blob/main/assets/Screenshot_4.png" width="400"> |

#### 📋 Interfejs Menu
| Główne Menu Misji | Wybór Aktu | Szczegóły Zadania | Szczegóły zadania z Bronią |
|:---:|:---:|:---:|:---:|
| <img src="https://github.com/AmxxPro-pl/Mission-System/blob/main/assets/Screenshot_2.png" width="250"> | <img src="https://github.com/AmxxPro-pl/Mission-System/blob/main/assets/Screenshot_3.png" width="250"> | <img src="https://github.com/AmxxPro-pl/Mission-System/blob/main/assets/Screenshot_6.png" width="250"> | <img src="https://github.com/AmxxPro-pl/Mission-System/blob/main/assets/Screenshot_7.png" width="250"> |

#### 🏆 Rankingi
| TOP 15 Najlepszych Graczy (MOTD) |
|:---:|
| <img src="https://github.com/AmxxPro-pl/Mission-System/blob/main/assets/Screenshot_8.png" width="600"> |

---

### ⚙️ Dokumentacja Techniczna (Pełna dokumentacja wraz z przykładami użycia po zakupie) / Documentation (Full documentation with usting examples after buy)

<details>
  <summary><b>I. Instalacja i Konfiguracja (Kliknij, aby rozwinąć)</b></summary>

#### Instalacja Głównego Silnika (CORE)
1. Plik `Misje_Pro.amxx` wgraj do `addons/amxmodx/plugins/`.
2. Folder `AmxxProPL` wgraj do `sound/`.
3. Dopisz `Misje_Pro.amxx` na samej górze pliku `plugins.ini`.
4. Po restarcie uzupełnij dane MySQL w `addons/amxmodx/configs/AmxxProPL/misje_pro.cfg`.

#### Formatu pliku .cfg
Każda linia misji musi zachować poniższy format:
`MISJA "TYP" "CEL" "NAGRODA_NAZWA" "WARTOSC_NAGRODY" "ID_BRONI" "TYTUL" "OPIS"`
</details>

<details>
  <summary><b>II. Typy Misji (Core + Addons)</b></summary>

**Core (Typy 1-12):**
1. Rozegraj X rund | 2. Zabij X osób | 3. Zabij X (HS) | 4. Zadaj X DMG | 5. Zadaj x DMG (HS) | 6. Paka C4 | 7. Podnieś Ammo | 8. Przetrwaj rundę etc...

**JailBreak (Typy 13-22):**
13. Zabij Prowadzących | 14. Zabij Prowadzących HS | 15. Zabij Strażników | ... | 21. Ostatni Więzień | 22. Życzenia

**CoD Mod (Typy 23-25):**
23. Zabij jako konkretna klasa | 24. Zadaj DMG jako konkretna klasa | 25. Awansuj o X poziomów
</details>

<details>
  <summary><b>III. Developer API (Natywy)</b></summary>
  
```
native get_user_mission_type(id);          // Zwraca ID typu zadania
native get_user_mission_desc(id, dest[], len); // Pobiera opis misji
native add_user_mission_progress(id, val); // Dodaje postęp
native skip_user_mission(id);              // Pomija misję
native get_user_completed_missions(id);   // Zwraca liczbę ukończonych zadań
native get_user_mission_weapon(id);        // Zwraca wymaganą broń
```
</details>
