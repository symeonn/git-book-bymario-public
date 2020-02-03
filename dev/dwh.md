---
description: everything about Data Warehouse
---

# DWH

## optymalizacja DWH

* jeśli nie ma wartości dla danych wymiarów to nie zapisujemy jej w fact żeby nie zajmowała miejsca \(może to zależeć od danych\)
* w dim tables potrzebne są ID \(żeby łączyć w FACT\), value \(żeby łączyć w transform\) i name \(żeby wyświetlać w filtrach\)
* if scalar in fact table will be null then it doesn't make sense to store it in fact table
* make export script for dim tables



## **Pytania przy tworzeniu raportów**

* koniecznie ustalić nazwę raportu - ta nazwa będzie później używana wszędzie
* na czy polega/co pokazuje raport - ogólnie
* jakie pola w fact\_table powinny się znaleźć i są potrzebne do raporty \(PBI\)
* jakie z tych pól będą wymiarami \(dim\_tables\)
* czy wszystkie pola są potrzebne \(ze względu na wydajność\)
* czy pre\_stage są potrzebne i jeśli tak to ile poziomów

## Budowanie DWH

* zacząć od jenkinsfile + job 
  * time\_marker
  * dim\_date
* dim\_\* tables \(na podstawie kolumn dostarczonych od produktu\)
* export scripts tylko dla dim 
* import scripts + pre\_\*/stage\_\* tables \(może niektóre pre\_\* nie są potrzebne\) 
* RUN jenskins job for testing, when no errors limit results for 100k for dev purposes
* transform tylko dla dim\_\*
* RUN
* transform dla fact \(fields will be settled\) then pre/stage\_  , and fact\_ table\(s\)
* hints for transform: get 2, 3 dims and apply them then create aggregates and check if values are correct then apply rest of dimensions nad check some values
* END
* * tabeli fact z wymaganymi polami i dimensions FK + wymagane tabele dim
* Jeśli dim\_table która jest enumem i nie ma odpowiedniej tabeli z której można eksportować - należy wartości wziąć se stage \(dla fact\) żeby mieć na pewno poprawne wartości
* export ze stage
* Jenkinsfile \(to test export nad load, transform later\)
* load
* transform

## Optimization

#### EXPORT

Do minimum number of joins possible.   
Export raw data and join it on the DWH side using stage tables

#### Transformata: 

albo: select from \[all dim tables\] i agregowanie z tabeli stage  
Można ograniczyć ilość wierszy z dim przez zawężenie wartości które występują w stage  
jeśli potrzebujemy subqueries  
  
  
np:  
dim\_school zamiast brać wszystkie szkoły to najpierw biorę wszystkie school\_id z tabeli stage\_logins i w transformacie robię where dim\_school.school\_id in \(schools\_id\)  




  
albo: select from stage + join dim tables  
Jeśli potrzebujemy proste agregaty i możemy zrobić group by

Jeśli jest więcej subqueries potrzebnych to wtedy select from all dims  
Jeśli jest więcej prostych agregatów to wtedy select from fact

It is maybe good idea to introduce another stage to first make transform with some subqueries and then another transform with simple aggregates  


