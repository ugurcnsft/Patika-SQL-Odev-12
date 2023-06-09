1#SORU - film tablosunda film uzunluğu length sütununda gösterilmektedir. Uzunluğu ortalama film uzunluğundan fazla kaç tane film vardır?

1#CEVAP - SELECT COUNT(length) FROM film 
WHERE length > 
( SELECT AVG(length) FROM film 
);

1# <img width="960" alt="1" src="https://github.com/ugurcnsft/Patika-SQL-Odev-12/assets/129968939/30c7af4b-6db0-406b-8c55-b5ee2cc501a8">

2#SORU - film tablosunda en yüksek rental_rate değerine sahip kaç tane film vardır?

2#CEVAP - SELECT COUNT(film) FROM film
WHERE rental_rate = 
(SELECT MAX(rental_rate) FROM film 
);

2# <img width="960" alt="2" src="https://github.com/ugurcnsft/Patika-SQL-Odev-12/assets/129968939/6208063a-7aa4-4d3c-8106-88485896552f">

3#SORU - film tablosunda en düşük rental_rate ve en düşün replacement_cost değerlerine sahip filmleri sıralayınız.

3#CEVAP - SELECT title FROM film 
WHERE rental_rate = (SELECT MIN(rental_rate) FROM film) 
AND replacement_cost = (SELECT MIN(replacement_cost) FROM film);

3# <img width="960" alt="3" src="https://github.com/ugurcnsft/Patika-SQL-Odev-12/assets/129968939/04be0f41-0c8f-4c70-a4f8-1a94b90e92cb">

4#SORU - payment tablosunda en fazla sayıda alışveriş yapan müşterileri(customer) sıralayınız.

4#CEVAP - SELECT COUNT(payment_id), customer_id FROM payment 
GROUP BY customer_id 
ORDER BY COUNT DESC;

4# <img width="960" alt="4" src="https://github.com/ugurcnsft/Patika-SQL-Odev-12/assets/129968939/dc33e5ec-626e-4f2a-b4b3-82532672cea8">
