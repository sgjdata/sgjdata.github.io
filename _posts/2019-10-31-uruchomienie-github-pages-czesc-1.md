---
layout: post
title:  "Uruchomienie bloga GitHub Pages #1"
date:   2019-10-31 18:30:00 +0200
author: sgjdata
categories: blog
tags: github github-pages
id: 2
---


Aby uruchomić blog na platformie GitHub Pages należy przejść następujące etapy:
1. Rejestracja na platformie GitHub
2. Utworzenie repozytorium *nazwa_użytkownika*.github.io
3. Instalacja Jekyll
4. Utworzenie i konfiguracja strony.
5. Publikacja w serwisie GitHub.

W dzisiejszym wpisie opiszę dwa pierwsze punkty z powyższej listy, które należy przejść, aby móc cieszyć się z posiadania własnej strony (bloga) w oparciu o GitHub Pages.


## Rejestracja na platformie GitHub

Utworzenie konta na GitHubie wymaga podania nazwy użytkownika, adresu e-mail oraz hasła do konta. 
Konieczne jest także wykonanie prostego zadania weryfikującego oraz zaakceptowanie warunków świadczenia usług i polityki prywatności.

Rejestracji konta można dokonać pod następującym adresem: 
[Dołącz do GitHub](https://github.com/join)



## Utworzenie repozytorium

Po rejestracji konta, należy utworzyć repozytorium, w którym będą przechowywane pliki naszego bloga. Repozytorium będzie oparte o system kontroli wersji [Git](https://git-scm.com/), co umożliwia m.in. przechowywanie pełnej historii dokonanych zmian, czy utrzymywanie równoległych wersji.

Aby utworzyć nowe repozytorium, z menu znajdującego się pod przyciskiem *"+"* należy wybrać funkcję *"New repository"*.

![]({{ site.baseurl }}/assets/images/2019/10/github-create-a-new-repository-1.png)

Zgodnie z przyjętą konwencją, nazwa repozytorium powinna się składać z nazwy użytkownika, kropki i rozszerzenia *github.io*. W moim przypadku będzie to *sgjdata.github.io*.

![]({{ site.baseurl }}/assets/images/2019/10/github-create-a-new-repository-2.png)

Po utworzeniu repozytorium będzię ono dostępne pod adresem [https://github.com/sgjdata/sgjdata.github.io](https://github.com/sgjdata/sgjdata.github.io). Natomiast sama strona będzie dostępna pod adresem [https://sgjdata.github.io/](https://sgjdata.github.io/) 

W tym momencie, po wejściu na tą stronę będzie się wyświetlał błąd 404, gdyż na serwerze nie została jeszcze umieszczona żadna treść. Aby to zmienić konieczna jest instalacja systemu Jekyll, następnie utworzenie w oparciu o niego strony, jej konfiguracja i publikacja w serwisie GitHub.

Dalszy etap opiszę w kolejnym wpisie.
