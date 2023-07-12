# Excel HR dashboard project

## Dashboard pro HR oddělení     


Odkaz na můj **Linkedln** [ZDE](https://www.linkedin.com/in/mat%C4%9Bj-frol%C3%ADk-183812230/) 

-------

### Úvod do projektu
Cílem projektu je zobrazit v grafech a tabulkách údaje o zaměstnancích společnosti.

### Jednotlivé kroky projektu
1. Úprava přidělených dat, příprava nových sloupců pro následné grafické zobrazení počtu odpracovaných let a počtu propuštěných a stále pracujících osob.


Navázání dvou tabulek (uzemi_kod pro obě dvě tabulky shodný, data_kraj znázorňuje tabulka obsahující kraje ČR dle územních kódů, č. 2 značí druhý sloupec obsahující názvy krajů):
```
=IFERROR(VLOOKUP([@[uzemi_kod]];data_kraj;2;FALSE);"neurceno")
```
Filtrování nulových hodnot, v dané tabulce souhrnné hodnoty po jednotlivá území:
```
=IF([@[stav_txt]]<>"";1;0)
```


### Grafické znázornění rodinného stavu v Čr a krajích v roce 2021

<br />

![My Image](pic/marital-cz.png)
![My Image](pic/marital-cz-p.png)
<br />

![My Image](pic/marital-dist.png)
![My Image](pic/marital-dist-p.png)

