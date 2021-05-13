---
# Front matter
lang: ru-RU
title: "Отчёт по лабораторной работе"
subtitle: "Лабораторная №4"
author: "Чупрына Петр Петрович"

# Formatting
toc-title: "Содержание"
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4paper
documentclass: scrreprt
polyglossia-lang: russian
polyglossia-otherlangs: english
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase
indent: true
pdf-engine: lualatex
header-includes:
  - \usepackage{lmodern}
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=700 # the penalty for breaking a line at a binary operator
  - \relpenalty=500 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=100 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Изучить уравнение гармонического осцилятора


# Задание

1.	Построить решение уравнения гармонического осциллятора без затухания
2.	Записать уравнение свободных колебаний гармонического осциллятора с затуханием, построить его решение. Построить фазовый портрет гармонических колебаний с затуханием.
3.	Записать уравнение колебаний гармонического осциллятора, если на систему действует внешняя сила, построить его решение. Построить фазовый портрет колебаний с действием внешней силы.

Постройте фазовый портрет гармонического осциллятора и решение уравнения гармонического осциллятора для следующих случаев

1. Колебания гармонического осциллятора без затуханий и без действий внешней
силы $\ddot{x}+3.7x=0$
2. Колебания гармонического осциллятора c затуханием и без действий внешней
силы $\ddot{x}+3\dot{x}+10x=0$
3. Колебания гармонического осциллятора c затуханием и под действием внешней
силы $\ddot{x}+3\dot{x}+11x=0.9sin(0.9t)$

На интервале $t \in [ 0;63 ]$, шаг 0.05, $x_0=0.1, y_0=1.1$

# Выполнение лабораторной работы

На итнтервале $t \in [ 0;63 ]$, шаг 0.05, $x_0=0.1, y_0=1.1$

1. В системе отсутствуют потери энергии (колебания без затухания) Получаем уравнение $$\ddot{x}+\omega_0^2x=0$$
Переходим к двум дифференциальным уравнениям первого порядка:
$$ \dot{x}=y \
\dot{y}=-\omega_0^2x$$

![График решения для случая 1](image\1.png){#fig:001 width=70%}

![Фазовый портрет для случая 1](image\2.png){#fig:002 width=70%}


2. В системе присутствуют потери энергии (колебания с затуханием)
Получаем уравнение
$$\ddot{x}+2\gamma\dot{x}+\omega_0^2x=0$$

$$\dot{x}=y \
\dot{y}=-2\gamma y-\omega_0^2x$$

![График решения для случая 2](image\3.png){#fig:003 width=70%}

![Фазовый портрет для случая 2](image\4.png){#fig:004 width=70%}


3.  На систему действует внешняя сила.
Получаем уравнение $$\ddot{x}+2\gamma\dot{x}+\omega_0^2x=F(t)$$
Переходим к двум дифференциальным уравнениям первого порядка:
$$ \dot{x}=y \
\dot{y}=F(t)-2\gamma y-\omega_0^2x$$

![График решения для случая 3](image\5.png){#fig:005 width=70%}

![Фазовый портрет для случая 3](image\6.png){#fig:006 width=70%}

# Вывод
В ходе выполнения работы я изучил построение решения уравнения гармонического осциллятора, фазового портрета гармонических колебаний без затухания, с затуханием, а также при воздействии внешней силы.