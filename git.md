``` ls ``` lista plików
``` ls -lthr ``` lista ze szczegółami




``` git init ``` tworzy repo w aktualnym katalogu

``` git init --bare ``` tworzy repozytorium bez katalogu roboczego (nie można edytować plików)

``` git clone <repo> ``` skolonowanie istniejącego repozytorium

``` git add <plik> ``` dodanie pliku do śledzenia (* doda wszystkie pliki)

``` git rm <plik>``` usuwanie pliku ze śledzenia

```git rm -r --cached <folder>``` usuwanie ze śledzenia i z serwera całego folderu

``` git commit -m "" ``` zatwierdzenie zmian (parametr -m to opis)

```git commit --amend -m "New commit message"``` modify existing, unpushed commits

```git reset --soft HEAD~1``` Delete the most recent commit, keeping the work you've done

``` git push ``` wypchnięcie wszystkich zatwierdzonych zmian do zdalnego repozytorium

``` git status ``` sprawdzenie stanu repozytorium

``` git status -s ``` sprawdzenie stanu repozytorium wersja kompaktowa

``` git log ``` pełna historia commitów

``` git log -n X ``` X commitów wstecz

``` git log --stat ``` historia ze statystykami

``` git log --oneline ``` historia ze statystykami

``` git branch ``` wyświetlenie wszystkich gałęzi w repozytorium

``` git branch -a ``` wyświetlenie wszystkich gałęzi w lokalnym i zdalnym repozytorium

``` git branch <nazwa> ``` utworzenie nowej gałęzi

``` git branch -d <nazwa> ``` usunięcie gałęzi

``` git checkout <nazwa> ``` przeniesienie do istniejącej już gałęzi

``` git checkout -b <nazwa> ``` utworzenie nowej gałęzi i przeniesienie się do niej

``` git checkout <ściezkaDoPliku> ``` odtworzenie pliku

```git checkout `git rev-list -n 1 --before="2017-04-21 00:00:00" master`  ``` przywrócenie stanu repo z konkretnej daty

``` git merge <nazwa> ``` łączenie aktualnej gałęzi z gałęzią o zadanej nazwie

``` git merge --no-ff <nazwa> ``` łączenie równoległych gałęzi - "3-way-merge"

``` git rebase ``` łączenie aktualnej gałęzi z możliwą modyfikacją historii

``` git rebase -i ``` interaktywny rebase pozwalający na modyfikację historii

 

#### połącznie istniejącego repo ze zdalnym serwerem

``` cd existing_repo_dir ``` 

``` git remote add origin git@github.com:reponame.git ```

``` git push -u origin master ``` 

 

#### konfiguracja

konfiguracja jest sumą ustawień w kilku plikach czytanych w kolejności:

```/etc/gitconfig``` w katalogu git (c:\Program Files\Git\etc\  lub c:\Program Files\Git\mingw64\etc\)

```~/.gitconfig``` w katalogu użytkownika (c:\Users\tr5872\)

```.git/config``` w katalogu projektu



``` git config -l``` listuje wszystkie wpisy konfiguracji
