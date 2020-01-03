---
layout: post
title:  "Uruchomienie bloga GitHub Pages #2"
date:   2020-01-03 23:25:00 +0200
author: sgjdata
categories: blog
tags: github github-pages git jekyll 
id: 3
---


W poprzednim wpisie opisałem proces rejestracji na platformie GitHub i utworzenia repozytorium dla bloga uruchomionego w oparciu o GitHub Pages . 


Wracam do tematu i w aktualnym wpisie opisuję ciąg dalszy, polegający na instalacji Jekyll, konfiguracji i przeniesieniu na platformę blogową.


## Instalacja Jekyll


Instalację systemu Jekyll wykonałem lokalnie - na komputerze pod kontrolą systemu Linux Ubuntu.

W pierwszym kroku zależało pobrać wymagane pakiety:

```shell
sudo apt-get install ruby-full build-essential zlib1g-dev
```

W następnym kroku, przygotowanie środowiska dla instalacji bibliotek (pakietów) dla języka Ruby, tzw. gemów.

```shell
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
```

Instalacja dla uproszczenia wykonywana w katalogu domowym. Konfiguracja taka pozwala na zarządzanie gemami bez posiadania uprawnień administratora.

Więcej informacji o gemach pod następującym adresem: 
[RubyGems Basics](https://guides.rubygems.org/rubygems-basics/)


Po wcześniejszym przygotowaniu, instalacja systemu Jekyll wykonywana przy użyciu poniższego polecenia:

```shell
 gem install jekyll bundler
```

<br />

## Utworzenie nowej strony (bloga)

Polecenia tworzące nową stronę (według domyślnego szablonu) i uruchamiające ją na lokalnym komputerze zostały przedstawione na poniższym listingu:

```shell
jekyll new myblog
cd myblog
bundle exec jekyll serve
```

Po uruchomieniu strona dostępna jest lokalnie  na porcie 4000:
`http://127.0.0.1:4000/`


Nowe wpisy przechowywane są w katalogu `_posts`. Domyślnie tworzony jest pierwszy powitalny wpis.

Do przechowywania wersji roboczych (draftów) służy katalog `_drafts`. Możliwe jest uruchomienie strony wraz z widokiem draftów - przy użyciu polecenia:
```shell
bundle exec jekyll serve --drafts
```
<br />

## Publikowanie strony na platfomie GitHub Pages


Opublikowanie blogu na platformie GitHub Pages polega na dodanie plików strony do odpowiedniego repozytorium GIT. Sprowadza się to do następującej sekwencji poleceń.

Inicjalizacja repozytorium GIT w katalogu z plikami strony:
```shell
git init
```

Dodanie plików i zatwierdzenie zmian:
```shell
git add .
git commit -m "first commit"
```

Ustawienie zdalnego repozytorium w serwisie GitHub:
```shell
git remote add origin https://github.com/sgjdata/sgjdata.github.io.git
```

Wysyłanie wykonanych zmian do zdalnego repozytorium:
```shell
git push -u origin master
```

Po wykonaniu powyższych poleceń, po chwili strona powinna być dostępna na platformie GitHub.