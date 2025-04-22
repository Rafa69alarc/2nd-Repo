# 2nd-Repo
2nd Repo SQL 
22/04/25
Nombre de serie, capítulo y ranking IMDB en forma descendente.

SELECT Series.titulo AS 'Título de la Serie',
       Episodios.titulo AS 'Título del Episodio',
       Episodios.rating_imdb AS 'Rating IMDB'
FROM Episodios
LEFT JOIN Series
ON Series.serie_id = Episodios.serie_id
WHERE Series.titulo = 'Stranger Things'
ORDER BY Episodios.rating_imdb DESC 
