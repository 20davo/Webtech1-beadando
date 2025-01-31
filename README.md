# Web technológiák 1 beadandó

## Készítette
Név: Szauter Dávid

Neptun kód: P4QKJP

## 1. Bevezetés
Ebben a dokumentációban a bemutatásra kerülnek a webes felületek kialakításai és megvalósításai. A beadandó témájának kiválasztásakor ötlet hiányában úgy döntöttem, hogy kombinálom a szakdolgozati projektemmel, amely szintén egy webes felület létrehozásáról és kialakításáról szól. Így nemcsak a tantárgy beadandó követelményeinek felelek meg, hanem továbbfejleszthetem a szakdolgozatomhoz kapcsolódó webalkalmazást is.

A projekt témája egy olyan JavaScript-alapú felület létrehozása volt, ahol egy FBDL formátumú kódot kellett a programnak átfordítania C nyelvre. Fontos, hogy a megoldás során kizárólag frontend megközelítést lehetett alkalmazni, így böngészőben könnyen elérhetővé vált az alkalmazás a felhasználóknak.

Mivel a projektet már korábban megvalósítottam, így tulajdonképpen azt felhasználva beleintegráltam a beadandóba.
A projektben több, már eleve létező JavaScript fájlt használtam fel a konverter működéséhez. A konverterhez készítettem egy saját logót is, ami egy letisztult, modern megjelenést ad a fordító programnak.

---

## 2. HTML elemei és CSS stílusai

Az elkészült projekt összesen 5 HTML fájlból és a hozzájuk tartozó CSS fájlokból áll. Az oldalakat próbáltam egységesre és könnyen olvashatóra kialakítani. Törekedtem a reszponzívitásra és a lehető legjobb felhasználói élményre. A sötétkék-fehér-világosszürke szineket használtam projekt alatt.

Az összes oldalon ugyanaz a navigációs menü található, kivéve a konverter oldalát, ahol a menü mellett a logó is megjelenik. Emellett minden oldal alján helyet kapott egy lábléc (footer), amely egységes megjelenést biztosít az oldalak számára.


### 2.1 `index.html` - Főoldal

Az `index.html` főoldal az alábbi HTML elemeket tartalmazza:
- **Navigációs sáv (`<nav>`)**: Az oldal főmenüje, amely linkeket tartalmaz a különböző oldalakra (`gallery.html`, `services.html`, `contact.html`, `fbdl_converter.html`).
- **Fő tartalom (`<main>` `<table> <tr> <th> <td>` `<ul> <ol>`)**: A projekt bemutatása. Táblázatok, számozott-, pontozott listák. A konverter logójára kattintva egy link vezet a program oldalára.
- **Üdvözlő szekció (`<h1> <p>`)**: Egy rövid bemutatkozó rész a konverterről és az FBDL-ről.
- **Lábléc (`<footer>`)**: Link a projekt Git repozitorjához.

Az `index_styles.css` bemutatása:
- **body**: Az alapstílusok meghatározása, mint a betűtípus (Arial, sans-serif), a háttérszín (#f5f5f5) és a szöveg színe (#333). Nincsenek margók és paddingek a teljes oldal megfelelő igazítása érdekében.
- **nav**: A navigációs menü egy sticky pozícióban helyezkedik el a képernyő tetején. A menü háttere sötétkék (#003971), a szöveg pedig fehér. A menüpontok lebegő effektust kaptak (hover állapotban a háttér világosszürke, a szöveg pedig kék lesz). Az aktív menüpontokat vastagított szöveggel és nagyobb betűmérettel emeltem ki.
- **main, h1**: A main elem maximális szélessége 1200px, középre igazítva (margin: 20px auto). Háttérszíne fehér, és kapott egy 8px-es lekerekített szegélyt, valamint egy dobozárnyékot az esztétikusabb megjelenésért. A h1 cím elem kapott egy 50px-es alsó margót az egyértelmű elválasztás érdekében.
- **table**:A táblázat 100%-os szélességű, így kitölti a rendelkezésre álló helyet.
A cellák és a táblázat 1px vastag, világosszürke (#ddd) szegélyt kaptak.
A fejléc (th) háttérszíne sötétkék (#003971), a szöveg pedig fehér, ezzel kiemelve a táblázat fejlécét.
A cellák 10px paddinget kaptak, hogy olvashatóbbak legyenek
- **footer**: A lábléc középre igazított (text-align: center).
A háttérszíne sötétkék (#003971), és a szöveg fehér.
A footer p bekezdések 14px-es betűméretet kaptak, hogy jól olvashatóak legyenek. A Git repo linkje kapott egy hover-underline effektet.

### 2.2 `services.html` - Szolgáltatások

A `services.html` oldal táblázatokat tartalmaz, amelyek különböző fejlesztői szolgáltatásokat mutatnak be. Az oldal szerkezete az alábbi főbb elemekből áll:

- **Navigációs menü**: Az oldal tetején található menüsor, amely linkeket biztosít a többi oldalhoz (`index.html`, `gallery.html`, `contact.html`, `fbdl_converter.html`).
- **Fő tartalom**: Az oldal címe *„Szolgáltatások”*, amely alatt egy több táblázat található az elérhető szolgáltatásokról és árakról.
- **Lábléc (footer)**: Az oldal alján található szokásos link a git repozitory-ra.

A táblázatok az alábbi HTML elemeket tartalmazzák:

- `<table>`: A táblázat maga, amelyben az adatok találhatóak.
- `<tr>`: Egy-egy rekord.
- `<th>`: A fejléc cellái, amelyek a táblázat oszlopainak címeit tartalmazzák.
- `<td>`: A táblázat tartalmi cellái.

Az oldal alján található egy link, amely a kapcsolatfelvételi oldalra mutat. Ez lehetővé teszi a látogatók számára, hogy ajánlatot kérjenek vagy további információt szerezzenek a szolgáltatásokról.

A `services_styles.css` fájl a táblázatok formázására ugyanazokat a megjelenítési szabályokat alkalmazza, mint az `index_styles.css`. A táblázatok teljes szélességben jelennek meg, a cellák világosszürke (#ddd) szegéllyel és 10px-es paddinggel rendelkeznek. A fejléc (th) sötétkék háttérszínt (#003971) és fehér szöveget kapott.

**offer class**: A link alapértelmezetten vastagított és nagybetűs, valamint sötétkék színű (#003971). Ha az egérrel fölé viszzük a kurzort, a háttér sötétkékre vált, a szöveg pedig fehér lesz.

### 2.3 `gallery.html` - Képgaléria

A `gallery.html` oldalon találhatók a konverterről készített képernyőképek valamint a program logója.
Az oldal szerkezetében nem tér el a többi oldaltól és a HTML és CSS fájlok tekintetében teljesen megegyezik.

### 2.4 `contact.html` - Kapcsolatfelvételi űrlap

A `contact.html` oldal egy interaktív kapcsolatfelvételi űrlapot tartalmaz a követelményeknek megfelelően, illetve a szokásos fejléc, lábléc elemeket.
Az **űrlap** HTML elemei:
- Név (`<input type="text">`) – kötelező kitölteni
- E-mail (`<input type="email">`) – kötelező kitölteni
- Üzenet (`<textarea>`) – szabad szöveges beviteli mező, kötelező kitölteni
- Színválasztó (`<input type="color">`) – lehetőséget biztosít a felhasználónak a kedvenc színük kiválasztására
- Dátumválasztó (`<input type="date">`) – a születési dátumot lehet itt megadni
- Feliratkozás (`<input type="checkbox">`) – a felhasználók feliratkozhatnak a hírlevélre
- Nem választása (`<input type="radio">`) – „Férfi” vagy „Nő” opciók kiválasztására szolgál, kitöltése kötelező
- Küldés (`<button type="submit">`) – gomb, az űrlap elküldésére

`contact_styles.css` tartalmazza a kapcsolatfelvételi lap formázásait és stílusait (több stílus a korábbiaknak megfelelően):

**form (űrlapok)**:
- Keret nélküli kialakítás (border: none;)
- Maximális szélesség: 550px
- Padding és belső térközök az elemek jobb olvashatósága érdekében
- Címkék (label) és beviteli mezők (input, textarea) megjelenítése blokk szinten.

**input, textarea, button (űrlapmezők és gombok)**:
- Szélesség: 100%, hogy teljesen kitöltsék a form területét
- Padding: 10px az olvashatóság érdekében
- Kerekített szegély (border-radius: 5px;)
- Szegély: Világosszürke (border: 1px solid #ccc;)
- Fókusz állapotban fekete szegély (border: 1px solid black;)
- A textarea mező magassága: 150px.

**button (Küldés gomb):**
- Alap háttérszín: Sötétkék (#003971)
- Szöveg színe: Fehér
- Lekerekített sarkok és nagyobb betűméret a kiemelés érdekében
- Hover állapotban sötétebb kék (#02274c)

### 2.5 `fbdl_converter.html` - A konverter oldala

Az `fbdl_converter.html` maga a konverter oldala, a program, ami végzi a C kód generálását. 

Főbb HTML elemek:
- **Navigációs menü**: Az oldal tetején található, és minden oldalra navigációt biztosít. A többi menütől abban tér el, hogy tartalmazza a konvertel logóját a bal felső sarokban.
- **Szerkesztő mező** (`<textarea>`): A felhasználók ide írhatják vagy másolhatják be az FBDL kódjukat. (egy alapértelmezett FBDL kódot tartalmaz)
- **Convert** gomb (`<button id="convertButton">`): Megnyomásával elindul a konvertálás.
- **Copy** gomb (`<button id="copyButton">`): Az outputot a vágoólapra másolja.
- **output** mező (`<pre id="resultOutput">`): Itt jelenik meg az átalakított C kód.
- **Szimulációs szekció**: Lehetővé teszi a kód tesztelését egy interaktív felületen.

`converter_styles.css` (szerkezete hasonlóan a korábbi oldalakhoz):

**Input mező és kimeneti terület** (#converterSection, #outputSection pre):
- Elrendezés: Grid alapú kialakítás, három oszlopos elrendezés
Háttérszín: világos szürke (linear-gradient(to bottom, #ffffff, #f1f1f1))
- Padding: 40px, lekerekített sarkok (border-radius: 15px)
- Árnyékolás (box-shadow: 0 10px 20px rgba(0, 0, 0, 0.15))
- Kimeneti mező (#outputSection pre):
    * Szegély: világosszürke (#ddd)
    * Betűtípus: Courier New, monospace
    * Maximális magasság: 430px, görgethető tartalom

**Gombok** (button)
- Alapértelmezett háttérszín: Sötétkék (#003971)
- Szövegszín: Fehér
- Lekerekített sarkok (border-radius: 8px)
- Hover állapotban:
    * Háttérszín: sötétebb kék (#025994)
    * Effekt: enyhe nagyítás (transform: scale(1.05))
    * Aktív állapotban (:active): a gomb kissé összehúzódik (transform: scale(0.95))

**Szimulációs szekció** (.simulation)
- Háttérszín: világosszürke (#f9f9f9)
- Szegély: 1px solid #ccc
- Lekerekített sarok (border-radius: 5px)
- Csúszkák (#sliders) és egyéb interaktív elemek tárolására szolgáló konténer

---

## 3. JavaScript (`converter.js`)

A `converter.js` fájl felelős az **FBDL konverter** működéséért, amely az **FBDL formátumú kódot** C nyelvre alakítja át (konvertálja). Az alábbiakban bemutatom a főbb funkcióit és működését.

### **Főbb funkciói**
1. **Beviteli mezők kezelése**  
   - Az FBDL kód egy **textarea** mezőben (`#codearea`) adható meg.
   - Az átalakított C kód egy `<pre id="resultOutput">` mezőben jelenik meg.

2. **Konvertálás indítása (`convertButton`)**
   - Az `#convertButton` gomb lenyomására meghívódik a **convertFBDLToC()** függvény, amely feldolgozza a beírt FBDL kódot.

3. **Kimenet másolása (`copyButton`)**
   - Az `#copyButton` gomb lehetővé teszi a generált C kód vágólapra másolását.
   - Ha nincs kimenet, figyelmezteti a felhasználót az esetleges hibákról.

### **Konvertálás logikája (`convertFBDLToC()`)**  
A konvertálás során:

1. **Tokenizálás**  
   - Az FBDL kód először **tokenizálásra** kerül a `tokenizeFBDL(fbdlCode)` függvény segítségével.
   - A `Tokenizer` osztály felelős az FBDL nyelvtani elemeinek felismeréséért.

2. **Univerzumok és szabálybázisok létrehozása**  
   - Az FBDL kód **univerzumokat (`universe`) és szabálybázisokat (`rulebase`)** tartalmaz.
   - A `processUniverse()` és `processRulebase()` függvények feldolgozzák ezeket az elemeket és utána generálják a megfelelő C kódot.

3. **C kód generálása**  
   - Az univerzumok és szabályok átalakítása után a C kód az `int main(){}` függvény segítségével kerül legenerálásra.
   - A `generateInputData()` függvény biztosítja, hogy az FBDL változók megfelelően beállításra kerüljenek a C kódban.

### **Hibakezelés**
- Ha a konvertálás során szintaktikai hiba lép fel, a konzolban részletes hibaüzenet jelenik meg (`console.error()`).
- Az `ERROR_CODE = -1` értéket használja a program hiba esetén.

### **Interaktív funkciók**
- A szimulációs szekció (`#simulationSection`) csúszkák (`sliders`) és visszajelző elemek (`indicators`) segítségével jeleníti meg a változók értékeit.

---

## 4. Összegzés

Az oldalak tervezésénél fontosnak tartottam a modern és egységes kinézetet, valamint a felhasználóközpontú elrendezést. Az oldalak sajnos nem teljesen reszponzívnak, de igyekeztem annak is megfelelni, valamilyen szinten.

A projekt eredeti dokumentációja (szakdolgozat gitrepója) és kódjai megtalálhatóak az alábbi [linken](https://github.com/20davo/FBDL-converter). 
