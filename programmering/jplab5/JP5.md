
## DAT100: Java Programmering 5 - Uke 38

**Bemerk** Oppgave O1-A nedenfor vil være en del av en obligatorisk innlevering med frist i starten av uke 40.

## Grunnleggende oppgaver

Koden i oppgavene nedenfor skrives inn i klasse `G` med en `main`-metode som vist nedenfor.

```java
public class OppgaveG {

	public static void main(String[] args) {

    // TODO - legg til tabeller og metodekall her

	}

  // TODO - legg til deklarasjon av metoder her

}
```

Som del av oppgaven bør du videre teste at koden og metodene som implementeres fungerer. Dette kan eksempelvis gjøres ved å skrive ut verdien i consollen.

### Oppgave G1: Tabeller

#### a)

Legg inn en tabell med heltal `int[] tabell = {1, 3, 4, 7, 9, 10}` i main-metoden.

#### b)

Legg til kode i main-metoden som skriver ut innholdet/verdien som står på posisjon `2` i tabellen (riktig svar er 4).

#### c)

Legg til kode i main-metoden som endrer innholdet som er lagret på posisjon 2 fra verdien 4 til verdien 7.

#### d)

Legg til kode i main-metoden som skriver ut innholdet av tabellen ved bruk av en for-løkke med indeks.

#### e)

Flyt koden fra d) ut i en egen metode `public static void skrivUt(int[] tab) ` som kan skrive ut innholdet av en tabell. Kall `skrivUt`-metoden fra main-metoden.

#### f)

Modifiser metoden fra e) slik den bruker en utvidet for-løkke.

#### g)

Skriv en metode `public void finnes(int[] tabell, int tall)` som returnerer `true` om `tall` finnes i tabellen og `false` ellers. Bruk en while-løkke.

#### h)

Skriv en metode `public int[] skiftfortegn (int[] tabell)` som returnerer en ny tabell som er identisk med tabellen gitt med som parameteren med hvor alle verdier har fått endret fortegn.

## Basisoppgaver

### Oppgave B1: Repetisjonsløkke og matematiske funksjoner

Ved å bruke Math-klassen får du tilgang til matematiske funksjoner som sinus og cosinus ved å bruke `Math.sin(x)` og `Math.cos(x)` i koden. Når du f.eks. skal regne ut verdien `y = sin(x)`, må *x* være i *radianer*.

Omregning mellom grader og radianer gjør du ved formelen:

vinkel i radianer = (π * vinkel i grader) / 180

Verdien π finst i Math-klassen som konstanten `Math.PI`.

Alternativ kan du bruke en innebygd metode i Math-klassen for dette. Se dokumentasjonen for Math-klassen (http://docs.oracle.com/javase/8/docs/api/index.html) for å finne metoden for omregning mellom grader og radianer.

Lag en enkel klasse der du i main-metoden skriver ut en tabell over sinus og cosinus til alle vinkler mellom 0 og 180 grader, i steg på 15 grader.

Utskriften kan f. eks. se slik ut:

```
  x i grader  x i radianer    sin(x)    cos(x)
------------------------------------------------
           0         0.000     0.000     1.000
          15         0.262     0.259     0.966

          ..            ..        ..        ..

         180         3.142     0.000    -1.000
------------------------------------------------
```

Prøv å løse oppgaven både ved å bruke en for-løkke og etterfølgende ved å bruke en while-løkke.

### Oppgave B2: Metoder og løkker

Se på programmet nedenfor som leser inn to tall (en høyde og en bredde) og beregner areal via metoden `private static int areal(int bredde, int hoyde)`

```java

public class InputAreal {

	public static void main(String[] args) {

		String breddeStr = showInputDialog("Bredde:");
		int bredde = parseInt(breddeStr);

		String hoydeStr = showInputDialog("Høyde:");
		int hoyde = parseInt(hoydeStr);

		int a = areal(bredde,hoyde);

		showMessageDialog(null,"Areal: " + a);
	}

	private static int areal(int bredde, int hoyde) {

		int flateareal = bredde * hoyde;

		return flateareal;
	}

```

##### a)

Utvid klassen ovenfor med en metode `private static int lesInnTall(String message)` som leser inn et tall via `showInputDialog` og returner heltallverdien. Parametren `message` er den tekst som skal vises i dialogboksen.

##### b)

Modifiser main-metoden i programmet ovenfor slik den bruker metoden fra a) til å lese inn høyde og bredde.

##### c)

Utvid metoden `lesInnTall` fra a) slik metoden fortsetter med å lese inn et tall inntil tallet er positivt. **Hint:** bruk en do-while løkke.

### Oppgave B3 - Løkker

Java-boken Kap. 3 oppgave 13

### Oppgave B4 - Tabeller og decimaltall

Du skal lage et program for å lese inn temperaturen i Bergen for et bestemt klokkeslett for alle dager i en bestemt uke (dvs. 7 temperaturer).

**Temperaturer skal lagres i en tabell**.

Programmet skal videre finne og skrive ut gjennomsnittet av disse verdiene og den høyeste temperaturen for hele uken.

Skjermdialogen kan se ut som eksempelet nedenfor:

```
Analyse av temperaturer
***********************     
Skriv inn temperaturene:
1. dag: 22.2
2. dag: 21.5
3. dag: 26.5
..
7. dag: 18.3

Gjennomsnittstemperaturen var 22.1
Maksimum for denne uken var 26.5 grader
```

### Oppgave B5

Java-boken Kap. 3 oppgave 14

## Obligatoriske oppgave O1-A

Denne oppgaven omhandler tabeller og metoder og vil være en del av neste obligatorisk innlevering med frist i starten av uke 40.

Den obligatoriske innleveringen skal gjøres i grupper med opptil 4 personer. Det er de **samme gruppene** som dere skal bruke i programmeringsprosjektet i uke 41/42.

**Husk** å bruke startkoden og enhetstester for oppgaven:

https://github.com/dat100hib/dat100-javainnlevering2/blob/master/README.md

På siden ovenfor er det også beskrevet hvordan dere kan clone startkoden til egen PC og hvordan dere kan utføre enhetstestene.

Metodene i denne oppgaven skal implementeres fra bunden og det er derfor **ikke** lov å bruke metoder som finnes i Arrays-klassen.

##### a)

Implementer en metode:

```java
public static void skrivUt (int[] tabell)
```

som kan skrive ut en tabell med heltal. Du kan selv bestemme formatet.

##### b)

Implementer en metode:

```java
public static String tilStreng (int[] tabell)
```

som kan returnere en tekststreng (String) med innholdet av en tabell. For en tabell med elementene 42,67,89 skal følgende streng returneres:

```java
"[42,67,89]"
```

##### c)

Implementer en metode

```java
public static int summer (int[] tabell)
```

som gitt en `tabell` av heltall som parameter beregner summen av tallene som er lagret i tabellen.

Implementer tre varianter av metoden: en som bruker en vanlig for-løkke, en som bruker en while-løkke, og en som bruker en utvidet for-løkke.

Test de ulike implementasjoner av metoden på utvalgte tabeller og se at de gir riktig resultat. Metoden fra a) kan brukes ifm. test.

##### d)

Implementer en metode

```java
public static boolean finnesTall (int[] tabell, int tall)
```

som gitt en `tabell` og et tall returnerer `true` om tabellen `tabell` innholder tallet `tall` og `false` ellers.

##### e)

Implementer en metode

```java
public static int posisjonTall (int[] tabell, int tall)
```

som returnerer det første index (posisjon) i `tabell` som inneholder tallet `tall` og `-1` ellers.

##### f)

Implementer en metode

```java
public static int[] reverser(int[] tabell)
```

som gitt en `tabell` av heltall returnerer en ny tabell som har de samme elementene som `tabell` men i modsatt rekkefølge.

##### g)

Implementer en metode:

```java
public static boolean erSortert (int[] tabell)
```

som kan avgjere om ein array (tabell) av heiltal er sortert stigande (dvs. at alle tal skal vere større enn det forrige)

##### h)

Implementer en metode:

```java
public static int[] settSammen(int[] tabell1,int[] tabell2)
```

som gitt to tabeller `tabell1` og `tabell2` som parametre og returnerer en ny tabell som er sammensetning av de to tabeller.
