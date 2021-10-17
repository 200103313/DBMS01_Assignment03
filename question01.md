SELECT DISTINCT Track.TrackId, Track.Name, Track.UnitPrice, Genre.Name
FROM Track, Genre
WHERE Track.GenreId = Genre.GenreId
ORDER BY Track.Name

---------------------------------------

SELECT Genre.Name, COUNT(*) AS c
FROM Track, Genre
WHERE Genre.GenreId = Track.GenreId 
GROUP BY Genre.Name
HAVING COUNT(*) > 100
