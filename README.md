# Zarządzanie Cyklem Życia Aplikacji

Repozytorium związane z przedmiotem **Zarządzanie cyklem życia aplikacji** służące nauce zarządzania kodem przy użyciu **sytemu kontroli wersji Git**.

Projekt obejmuje:

- instalację Git,
- inicjalizację repozytorium Git,
- śledzenie zmian w repozytorium,
- ustawienie referencji repozytorium lokalnego do zdalnego,
- synchronizację repozytorium lokalnego z repozytorium zdalnym,
- ręczne rozwiązywanie konfliktów,
- zarządzanie branchami.

---

## #1 Instalacja

- Windows: https://gitforwindows.org/

## #2 Konfiguracja

    git config --global user.name "FirstName LastName"

    git config --global user.email "email@example.com"

## #3 Praca z repozytorium

- Inicjalizacja repozytorium.

      git init

- Ustawianie adresu zdalnego repozytorium.

      git remote add origin url_repozytorium

- Klonowanie zdalnego repozytorium.

      git clone url_repozytorium

- Sprawdzanie aktualnego stanu repozytorium.
    
      git status

- Sprawdzanie historii zatwierdzonych zmian.
    
      git log

## #4 Śledzenie, zatwierdzanie i wysyłanie zmian na serwer

- Śledzenie zmian (dodawanie i usuwanie plików ze staging area).

    - Dodawanie wszystkich plików.

          git add -A

    - Dodawanie wyłącznie nowych plików i tych, które zostały zmodyfikowane

          git add .

    - Dodawanie wyłącznie usuniętych plików i tych, które zostały zmodyfikowane

          git add -u

    - Usuwanie śledzonych plików.

          git restore --staged nazwa_pliku_1 nazwa_pliku_2

- Zatwierdzanie zmian.

    - Zatwierdzanie wszystkich śledzonych plików.

          git commit -m "Komentarz dotyczący wprowadzonych zmian."

    - Zatwierdzanie zmain dla konkretnych śledzonych plików.

          git commit -m "Komentarz dotyczący wprowadzonych zmian." nazwa_pliku_1 nazwa_pliku_2

- Wysyłanie wprowadzonych zmian na serwer.

      git push origin master

      git push

- Synchronizowanie repozytorium zdalnego z lokalnym.

      git pull origin master

      git pull

## #5 Zarządzanie branchami

- Sprawdzanie aktualnie isteniejących branchy.

      git branch

- Tworzenie brancha.

      git branch nazwa_brancha

- Zmiana aktualnego brancha.

      git checkout nazwa_brancha

- Usuwanie brancha lokalnie.

      git branch -d nazwa_brancha

- Usuwanie brancha zdalnie (w zdalnym repozytorium).

      git push url_repozytorium --delete nazwa_brancha

- Mergowanie branchy.

      git merge nazwa_brancha_ktory_chcemy_zmergowac_z_aktualnym