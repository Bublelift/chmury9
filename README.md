# Zadanie 9.2
Wykonanie usługi LEMP na kontenerach Docker

# PHP
Oficjalny obraz php w wersji 8.0.18. Kontener podłączony jest do sieci *backend*.
Podłączony jest do niego folder, w którym jest plik index.php, który wypisuje
informacjie o php.

# Nginx
Najnowszy obraz nginxa, wystawiony na porcie 6666. Kontener podłączony jest do sieci
*backend* oraz *frondtend*. Podłączone są do niego plik konfiguracyjny oraz wyżej
wymieniony folder. Kontener jest zależny od kontenera *PHP*.

# MySQL
Oficjalny obraz MySQL. Kontener podłączony jest do sieci *backend*. Będzie zawsze
restartował się w przypadku błędu. Podłączony do niego jest wolumen o nazwie *mysql_vol*.
Domyślnym hasłem jest *root*, a domyślną bazą danych *test_db*.

# PHPMyAdmin
Kontener umożliwia zarządzanie bazą danych. Jest zlinkowany z kontenerem bazy danych.
Wystawiony jest na zewnątrz poprzez port 6001. Podłączony do sieci *backend*.

# Wolumeny
Utworzony jest jeden wolumen dla kontenera bazy danych: *mysql_vol*.

# Sieci
Utworzone zostają 2 sieci, *frontend* i *backend*.