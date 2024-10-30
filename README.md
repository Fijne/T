###################################################################
###### Sitzung 1                                          #########
###### Einführung in die Psychologische Methodenlehre     #########
###### Lukas A. Knitter, Wintersemester 2024/2025         #########
###################################################################

# Überblick über die Themen:
# - Einfache Berechnungen
# - Variablen
# - Datentypen und Vektoren
# - Funktionen
# - Kommentare und Dokumentation
# - Arbeitsverzeichnis
# - Speichern von Objekten

## ---- Einfache Berechnungen ----
# R kann wie ein Taschenrechner verwendet werden:
5 + 3  # Addition
12 - 4  # Subtraktion
6 * 7  # Multiplikation
20 / 5  # Division
11^2 # Potenzieren

## ---- Variablen ----

# Variablen speichern Objekte, die später wiederverwendet werden können.
# Mittels Zuweisungsoperator <- werden Objekte einer Variable zugewiesen
x <- 10  # Zuweisung des Werts 10 an die Variable x
y <- 7   # Zuweisung des Werts 7 an die Variable y

# Jetzt können wir Berechnungen mit diesen Variablen durchführen:
x + y  # Addition
x * y  # Multiplikation

## ---- Datentypen ----
# Zahlen (numeric)
num <- 42
class(num)  # Überprüfen des Datentyps

# Zeichenketten (character)
text <- "Hallo R!" # Zeichenketten müssen von " oder ' umgeben sein.
class(text)  # Überprüfen des Datentyps

# Logische Werte (logical)
is_true <- TRUE
class(is_true)  # Überprüfen des Datentyps

## ---- Uebungsaufgabe 1 ----
# Erstellen Sie zwei Variablen mit den Namen "anfang" und "ende". 
# Weisen Sie diesen Variablen jeweils den ersten und letzten Buchstaben ihres eigenen Namens zu.
# Addieren Sie die beiden Variablen. Was passiert?

## ---- Vektoren ----
 
# Erstellen eines character Vektors
letters <- c('a','b','c')
letters # Die Ausgabe erfolgt durch das Ausführen des Objektnamens.

# Erstellen eines numerischen Vektors
numbers <- c(1, 2, 3, 4, 5)
numbers  # Ausgabe des Vektors

# Erstellen eines numerischen Vektors, der eine Sequenz ganzzahliger Zahlen enthalten soll
numbers2 <- c(5:10)
numbers2  # Ausgabe des Vektors

# Zugriff auf einzelne Elemente im Vektor (indizieren):
numbers[1]  # Erstes Element
numbers[3]  # Drittes Element

# Indizieren funktioniert auch mit character Vektoren:
letters[1]  # Erstes Element
letters[3]  # Drittes Element

# Mathematische Operationen auf Vektoren:
numbers * 2  # Alle Elemente werden mit 2 multipliziert

## ---- Uebungsaufgabe 2 ----
# Erstellen Sie einen Vektor, der die beiden Zahlen 1 und 2 sowie die beiden Buchstaben a und b enthält.
# Was passiert?

## ---- Eingebaute Funktionen ----
# R bietet viele eingebaute Funktionen, um Berechnungen auf Daten durchzuführen.
# Funktionen haben immer die Struktur function(argument1,...)
# Beispiele: `c()`, `sum()`, `mean()`, `length()`.

# Berechnung des Mittelwerts:
mean(numbers)

mean(c(1,3,7)) 



# Berechnung der Summe:
sum(numbers)

# Anzahl der Elemente im Vektor:
length(numbers)

# Funktionen können auch innerhalb anderer Funktionen aufgerufen werden:
length(mean(numbers))

## ---- Uebungsaufgabe 3 ----
# Erstellen Sie zwei Variablen mit den Namen "Vorname" und "Nachname". 
# Weisen Sie diesen Variablen jeweils ihren eigenen Vor- und Nachnamen zu. 
# Verwenden Sie die Funktionen mean() und length() auf diese Variablen. 
# Was passiert jeweils?

## ---- Dokumentation ----

# Zu jeder Funktion gibt es eine ausführliche Dokumentation, die ihren Zweck und Funktionsweise erläutert.

?c() # Mittels ? Oberator vor einer Funktion oder
help(c) # Mittels help() Funktion kann die Dokumentation im "Help"-Fenster von R-Studio geöffnet werden

## ---- Kommentare ----

# Das ist eine Kommentarzeile

mean(c(21, 24, 27, 29)) # Auch das hier ist ein Kommentar

# sum(c(21, 24, 27, 29)) Dieser Befehl wird nicht ausgeführt

## ---- Arbeitsverzeichnis ----
# Im Arbeitsverzeichnis sucht und speichert R Daten

path.expand("~") # mithilfe dieser Funktion, können Sie herausfinden welcher Pfad hinter der Tilde steckt

setwd() # mithilfe dieser Funktion kann das Arbeistverzeichnis geändert werden

## ---- Objekte speichern ----
save.image(file="meineDaten.RData") # speichert alle Objekte der Environment im aktuellen Arbeitsverzeichnis
saveRDS(numbers, file="meineDatei.rds") # speichert das Objekt im aktuellen Arbeitsverzeichnis


