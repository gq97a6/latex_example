# LaTeX
Wprowadzenie do `LaTeX`-a oraz przykładowy projekt.

### Co mi to da?
- proste w obsłudze
- łatwe wprowadzanie globalnych zmian
- konsystencję wyglądu w całej pracy
- możliwość śledzenia zmian git-em
- autogenerowanie spisu treści

### Jak to działa?

Piszesz pracę w podobnym stylu do programowania a kompliator zamienia to do pliku PDF.

```latex
\documentclass[12pt]{article}

\begin{document}

\section{Section}

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

\subsection{Subsection}

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.

\subsubsection{Subsubsection}

\emph{Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.}

\end{document}
```

### Co jest potrzebne?
Najprostszą metodą jest skorzystanie z edytora online: https://www.overleaf.com/

Możesz też skonfigurować własne środowisko. Do tego przyda się:

1. `LaTeX Workshop`: https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop
- dodaje wsparcie dla `LaTeX`
- podgląd na żywo
- automatyczna kompilacja przy zapisaniu
- linter i intellisense

2. `MikTex`: https://miktex.org/
- kompilator
- automatyczne ściąga includowane biblioteki

3. `Perl`: https://strawberryperl.com/
- używany przez MikTex

### Dodatkowe informacje
- Po kompilacji generowane jest wiele plików, są one zbędne wiec nie warto ich dodawać do repozytorium.
- Pracę można podzielić na odzielne pliki/rozdziały i potem je importować do głównego pliku.
- Niektóre znaczniki działają podobnie do funkcji, mogą posiadać parametry, inne znaczniki wpływają na wszystko co jest po nich. Dla przykładu `\emph{Tekst}` tworzy napis z kursywą, a `\tiny` zmienia rozmiar czcionki na stałe.
- Powtarzalne części pracy warto wydelegować do odzielnych funkcji dla przejrzystości. Przykładowo funkcja która tworzy tabelę wymagania lub wpis w bibliografi.
- Podobnie jak `Markdown` `LaTeX` nie rozpoznaje znaku nowej lini jako nową linię. Można ją wymusić używając `\\`.
- `LaTeX` obsługuje wiele jednostek długości. Więcej na ten temat tutaj: https://www.overleaf.com/learn/latex/Lengths_in_LaTeX

### Przydatne znaczniki
- `\newpage` - wymusza nową stronę
- `\include{includes/1-wstep}` - dodaje rozdział z innego pliku
- `\setlength{\parindent}{0pt}` - nadpisuje zachowanie istniejących znaczników. W tym przypadku usuwa defaultowe wcięcie dla nowych paragrafów.
- `\section{A}` | `\subsection{B}` | `\subsubsection{C}`- tworzy nowe sekcje. Na ich podstawie tworzony jest spis treści
- `\vspace{5em}` - tworzy pionowy odstęp
- `\hspace*{0.5em}` - tworzy poziomy odstęp
- `\color{white}` - ustawia kolor czcionki
- `\pagecolor{black}` - ustawia kolor tła
- `\tableofcontents` - generuje spis treści
- `\setcounter{page}{0}` - ustawia licznik stron używany do automatycznego generowania stopki z numerem strony
