# examenDatabase

1. SELECT persoon_naam, persoon_voornaam FROM persoon WHERE persoon_naam LIKE 'm%' AND persoon_taal LIKE 'F'
2. SELECT persoon_id FROM persoon ORDER BY 1 DESC
3. SELECT product_code, product_nr FROM product WHERE locatie_nr IS NOT NULL
4. SELECT product_code, product_nr FROM product WHERE product_nr BETWEEN 5 AND 15 OR product_nr BETWEEN 30 AND 55
5. SELECT product_code, product_nr FROM product WHERE product_nr IN (5,10,20,25)
6. SELECT persoon_naam, persoon_voornaam FROM persoon WHERE RIGHT(persoon_naam,1) LIKE 's' AND (persoon_voornaam LIKE 'f%' OR persoon_voornaam LIKE'p%')
7. SELECT persoon_naam, persoon_voornaam, CASE persoon_geslacht WHEN 1 THEN 'man' WHEN 2 THEN 'vrouw' END persoon_geslacht, CASE persoon_taal WHEN 'N' THEN 'Nederlandstalig' WHEN 'F' THEN 'Franstalig' END persoon_taal FROM persoon
8. SELECT COUNT(persoon_id) FROM persoon WHERE persoon_taal LIKE 'F'
9. SELECT product_code, product_nr FROM product WHERE oorsprong_nr IS NULL
10. SELECT product_code, product_nr, COALESCE(locatie_naam,'') FROM product LEFT JOIN locatie ON product.locatie_nr = locatie.locatie_id
11. SELECT locatie_naam FROM locatie WHERE LENGTH(locatie_naam) = 16 AND locatie_naam LIKE 'magazijn%'
12. SELECT product_code, product_nr FROM product WHERE (product_code LIKE 'HA' OR product_code LIKE 'NE') AND product_nr < 15
13. SELECT product_code, product_nr FROM product WHERE (SELECT locatie_naam FROM locatie WHERE locatie.locatie_id = product.locatie_nr) LIKE 'maga%'
14. UPDATE product SET locatie_nr = 3 WHERE locatie_nr = 1
15. DELETE FROM product WHERE oorsprong_nr = 14
