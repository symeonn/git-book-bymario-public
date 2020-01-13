---
description: everything about Data Warehouse
---

# DWH

### optymalizacja DWH

* jeśli nie ma wartości dla danych wymiarów to nie zapisujemy jej w fact żeby nie zajmowała miejsca \(może to zależeć od danych\)
* w dim tables potrzebne są ID \(żeby łączyć w FACT\), value \(żeby łączyć w transform\) i name \(żeby wyświetlać w filtrach\)
* if scalar in fact table will be null then it doesn't make sense to store it in fact table
* make export script for dim tables
* **Pytanie przy tworzeniu raportów**
* koniecznie ustalic nazwę raportu - ta nazwa będzie później używana wszędzie
* jakie pola w fact\_table powinny się znaleźć i są potrzebne do raporty \(PBI\)
* jakie z tych pól będą wymiarami \(dim\_tables\)
* czy wszystkie pola są potrzebne \(ze względu na wydajność\)
* czy pre\_stage są potrzebne i jeśli tak to ile poziomów

## Budowanie DWH

* tabeli fact z wymaganymi polami i dimensions FK + wymagane tabele dim
* export ze stage
* Jenkinsfile \(to test export nad load, transform later\)
* load
* transform

