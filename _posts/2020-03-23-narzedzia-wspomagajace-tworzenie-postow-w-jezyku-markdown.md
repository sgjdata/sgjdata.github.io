---
layout: post
title:  "Narzędzia wspomagające tworzenie postów w języku Markdown"
date:   2020-03-23 20:25:00 +0200
author: sgjdata
categories: blog
tags: markdown jekyll pandoc joplin ide netbeans visual-studio-code
id: 4
---

W niniejszym poście opiszę sposoby tworzenia postów dla
bloga prowadzonego w oparciu o Jekyll i narzędzia wspomagające ten
proces. 

Wyróżnione zostaną następujące podejścia:

1.  Pisanie posta w procesorze tekstu i jego konwersja do Markdown przy
    użyciu konwertera dokumentów.
2.  Tworzenie posta bezpośrednio w języku Markdown przy użyciu edytora
    tekstu z obsługą tego języka.
3.  Tworzenie posta przy użyciu zintegrowanego środowiska
    programistycznego (IDE) z wbudowaną obsługą języka Markdown lub z
    zainstalowaną wtyczką temu dedykowaną.

Konwersja dokumentów przy użyciu Pandoc
---------------------------------------

Posty tworzone w procesorze tekstu (np. Microsoft Word, LibreOffice
Calc) wymagają konwertowania do języka Markdown. Tutaj z pomocą
przychodzi darmowy konwerter dokumentów [Pandoc](https://pandoc.org/).

Konwersja pliku w formacie ODT bezpośrednio do Markdown:

```shell
pandoc OdtFile.odt -o MarkDownFile.text
```

Konwersja pliku w formacie ODT pośrednio do HTML, a następnie do
Markdown:

```shell
pandoc OdtFile.odt -o HtmlFile.html
pandoc HtmlFile.html -o MarkDownFile.text
```


Edytory tekstu z obsługą składni Markdown
-----------------------------------------

Przy tworzeniu tekstów bezpośrednio w języku Markdown przydatny będzie
edytor tekstu obsługujący składnię Markdown.
Interesujące porównanie takich edytorów znalazłem na blogu Adeela Qayum
pod adresem: <br />
[The Ultimate List of the Best Markdown
Editors](https://www.oberlo.com/blog/markdown-editors)

### Joplin

Osobiście korzystam z aplikacji, której brakuje w powyższym porównaniu -
edytora [Joplin](https://joplinapp.org/). Aplikacja ta jest dedykowana
przede wszystkim tworzeniu notatek i listy zadań do wykonania. Jednak
wbudowana obsługa języka Markdown i wizualny pogląd ('na żywo')
wprowadzanego tekstu pozwala również stosować ją przy tworzeniu
blogowych postów.

![]({{ site.baseurl }}/assets/images/2020/03/joplin-application.png)


Tworzenie w zintegrowanym środowisku programistycznym (IDE)
-----------------------------------------------------------

Zintegrowane środowiska programistyczne lub edytory dedykowane
programistom oferują możliwość potraktowania bloga Jekyll jako projektu
programistycznego i pracę z blogiem jako takim.

Wsparcie dla Markdown może być wbudowane lub obsłużone przy użyciu
wtyczek.

Przykładowo, zintegrowane środowisko programistyczne NetBeans pozwala na
zainstalowanie obsługi języka Markdown przy użyciu wtyczki [Markdown
Support](http://plugins.netbeans.org/plugin/50964/markdown-support).
Wtyczka jest dostępna maksymalnie do wersji NetBeans 8.2.

Przydatnym narzędziem dla pracy ze składnią Markdown wydaje się być również edytor dla programistów [Visual Studio
Code](https://code.visualstudio.com/), który zawiera całą gamę
rozszerzeń zwraca następujące wyniki wyszukiwania dla
[Markdown](https://marketplace.visualstudio.com/search?term=markdown&target=VSCode&category=All%20categories&sortBy=Relevance).

Markdown Cheatsheet
-------------------

Dodatkowo polecam, dla osób niezaznajomionych ze składnią Markdown pomocna może
się okazać „ściągawka” dostępna na stronie [Markdown
Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).



