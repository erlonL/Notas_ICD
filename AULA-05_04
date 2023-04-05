# Scores

	Funções que mapeiam multiplos registros para um unico valor
	
	Exemplos:
	- notas atribuídas aos alunos;
	- IMC.
	
# Ranking
	
	Ordenando os resultados de uma função de score geramos um ranking
	
	Exemplos:
	- Ranking de alunos de uma turma de acordo com notas;
	- Sistema de recomendação de acordo com score de relevância do Netflix.

# Elo Ranking
	
	Em competições, rankings são criados fazendo comparações binárias;
	É criado a partir de comparações entre posições do ranking, por exemplo quando se ganha de um oponente em uma posição acima da sua, a posição sobe muito.
	
	- Começa avaliando todos os competidores igualmente;
	- A cada resultado de uma partida, o ranking é atualizado.
	
	
	## Fórmulas
	r'(A) = r(A) + k(SA - uA)
	
	uA = 1.Pa>b + (-1) (1- Pa>b)
	
	Pa>b depende da diferença de habilidade entre os competidores
	x = r(A) - r(B)
	
	função logit aplicada em x
	
# Aplicação de Elo Ranking
	```Python
	import math
	
	##
	def logit(x, c=0.4):
		1/(1+math.exp(-c*x))
		
	logit(-5)
	```
	##
	```Python
	def p(ranking_a, ranking_b):
		return logit(ranking_a - ranking_b)
	
	p(100,50)
	
	p(30,60)
	```
	def mi(p_ab):
		return p_ab - (1 - p_ab)
	
	mi(p(100, 50))
	mi(p(100, 120))
	
	def elo(ranking_a, ranking_b, s, k=10):
		p_ab = p(ranking_a, ranking_b)
		
		return ranking_a + k*(s-mi(p_ab))
	
	
	elo(100, 110, 1)
	
	p(100,110)
	
	mi(0)
	
	
	
	ranking = 100
	
	games_ranking = [110, 105, 90, 80, 120, 100]
	results = [1,1,-1,-1,1,-1]
	
	
	print('ranking: ', ranking)
	
	for i in range(len(games_ranking)):
		ranking = elo(ranking, games_ranking[i], results[i])
		print('ranking: ', ranking)
				
	
	ranking = 100
	
	print('ranking: ', ranking)
	
	for i in range(10):
		ranking = elo(ranking, 120, 1)
		print('ranking: ', ranking)
		
		
		
		
	
	
	```
	
