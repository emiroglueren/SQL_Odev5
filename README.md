# ODEV 5

Merhabalar,

Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

    film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en uzun (length) 5 filmi sıralayınız.
    film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en kısa (length) ikinci(6,7,8,9,10) 5 filmi(6,7,8,9,10) sıralayınız.
    customer tablosunda bulunan last_name sütununa göre azalan yapılan sıralamada store_id 1 olmak koşuluyla ilk 4 veriyi sıralayınız.

Kolay Gelsin.

# CEVAPLAR

## 1.Soru:

SELECT * FROM film
WHERE title LIKE '%n'
ORDER BY length DESC
LIMIT 5;

"Soldiers Evolution"
"Sorority Queen"
"King Evolution"
"Frontier Cabin"
"Wife Turn"

## 2.Soru:

SELECT * FROM film
WHERE title LIKE '%n'
ORDER BY length ASC
OFFSET 5
LIMIT 5;

"Jekyll Frogmen"
"Daughter Madigan"
"Room Roman"
"Camelot Vacation"
"Birds Perdition"

## 3.Soru:

SELECT * FROM customer
WHERE store_id = 1
ORDER BY last_name DESC
LIMIT 4;
