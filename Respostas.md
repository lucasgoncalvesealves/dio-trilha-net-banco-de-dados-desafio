# Respostas

1. SELECT nome, ano FROM Filmes

2. SELECT nome, ano FROM Filmes ORDER BY ano ASC

3. SELECT nome, ano, duracao FROM Filmes WHERE nome = 'De Volta para o Futuro'

4. SELECT * FROM Filmes WHERE ano = 1997

5. SELECT * FROM Filmes WHERE ano > 2000

6. SELECT * FROM Filmes WHERE duracao > 100 AND duracao < 150 ORDER BY duracao ASC

7. SELECT ano, COUNT(*) AS Quantidade FROM Filmes GROUP BY ano ORDER BY Quantidade DESC

8. SELECT PrimeiroNome, UltimoNome FROM Atores WHERE Genero = 'M'

9. SELECT PrimeiroNome, UltimoNome FROM Atores WHERE Genero = 'F' ORDER BY PrimeiroNome

10. SELECT Filmes.Nome, Generos.Genero FROM ((Filmes INNER JOIN FilmesGenero ON Filmes.Id = FilmesGenero.IdFilme) INNER JOIN Generos ON Generos.Id = FilmesGenero.IdGenero)

11. SELECT Filmes.Nome, Generos.Genero FROM ((Filmes INNER JOIN FilmesGenero ON Filmes.Id = FilmesGenero.IdFilme) INNER JOIN Generos ON Generos.Id = FilmesGenero.IdGenero) WHERE Generos.Genero = 'Mistério'

12. SELECT Filmes.Nome, Atores.PrimeiroNome, Atores.UltimoNome, ElencoFilme.Papel FROM
((ElencoFilme INNER JOIN Filmes ON ElencoFilme.IdFilme = Filmes.Id)
INNER JOIN Atores ON ElencoFilme.IdAtor = Atores.Id)
