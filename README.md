<div align=center>
  <img height="300" width="400" src="https://www.ufrn.br/resources/documentos/identidadevisual/logotipo/logotipo_flat.png">
  <h1 align="center">Banco de Dados Oracle para a base de dados de Bolsistas da UFRN</h1>
</div>
Todas as informações sobre o projeto se encontrará abaixo.<br>
🔨Projeto ainda em desenvolvimento.🔨
<h2>💽 Entidades:</h2>
Para se adequar às formas normais, foram criadas 9 entidades, cada uma com a sua chave primária de acordo com os 
Atributos disponibilizadas pela base e duas entidades associativas que receberão um código para cada relação. Assim, as entidades são:
	
- Grupo de pesquisa: conforme a base, ele tem o seu ID e nome, para cada grupo, terá seus discentes e docentes.
		
- Orientador: receberá o seu id da base, nome e a chave estrangeira do grupo à qual ele pertence.
		
- Aluno: criado para ter a posibilidade de ser adicionado alunos ingresssantes da universidade. Receberá os atributos
matricula e o nome do aluno.
		
- Bolsista: os seus atributos serão o ID do discente, matricula(FK da entidade aluno), 
ID orientador(FK de seu orientador) e ID grupo(FK do grupo à qual ele pertence).
		
- Unidade: receberá o ID unidade e o nome da unidade.
		
- Unidade aluno: é a entidade criada para relacionar a unidade com aluno, pois na ausência dela, os dados ficariam fora da forma normal. 
Nela terá os atributos matricula(FK de aluno) e ID unidade(FK de unidade), ambos serão primary, pois apenas eles já garantem a unicidade 
do registro.
		
- Projeto de pesquisa: receberá CD projeto(conforme base, é um código composto por letras e números), título, ano.
		
- Pesquisa: receberá ID pesquisa, CD projeto(FK de projeto), categoria, status, inicio pesquisa, linha pesquisa, fim(da pesquisa).
		
- Bolsa: esta entidade é para relacionar o bolsista com a sua pesquisa, garantindo a sua normalização, também e ao mesmo tempo ela foi 
ajustada para se relacionar com a entidade unidade, garantindo o funcionamento conceitual do banco. Os atributos dela serão cd bolsa, 
ID unidade(FK de unidade), ID pesquisa(FK de pesquisa), ID discente(FK do bolsista), cota e tipo bolsa. Esses dois últimos são da base,
colocado nesta entidade para se adequar conceitualmente.
 
<h2>📜 Conforme a análise dos dados, foram estabelecidas as seguintes RNs: 	</h2>

🚧 <b>Em construção...</b> 🚧
	
- Poderá ser armazenado diversos alunos da universidade, porém alguns deles são ou não comtemplados com a bolsa de 
Pesquisa, os que são, ganham um id especial como bolsista.

- Um aluno pode ou não ser bolsista, já está sendo considerada a posibilidade de ser cadastrado alunos que 
Possivelmente podem se tornar bolsistas.

- Grupo de pesquisa só se relacionará com os bolsista, pois não há alunos com pesquisas sem bolsas.
	
- Um bolsista pode ou não pertencer a um grupo

- Um bolsista deve ter um orientador.

- Um bolsista deve estar em uma ou muitas bolsas.

<h2>🛠 Tecnologias</h2>

As seguintes ferramentas foram usadas na construção do projeto:

- [Oracle SQL](https://www.oracle.com/br/database/sqldeveloper/)

<h2>📝 Licença</h2>

Este projeto esta sobe a licença MIT.
