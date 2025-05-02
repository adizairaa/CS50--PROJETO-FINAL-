🏨 Hotel Insights – Análise de Dados de Reservas
📋 Descrição
Hotel Insights é um aplicativo web desenvolvido para ajudar gestores hoteleiros a analisar dados de reservas de forma simples e visual. O projeto permite visualizar métricas importantes como ocupação, sazonalidade, receita e perfil de hóspedes, usando consultas em SQL e exibindo resultados através de gráficos interativos.

Este projeto foi criado como parte do projeto final do CC50, unindo conhecimentos de programação, análise de dados e SQL.

🚀 Funcionalidades
✅ Dashboard geral:

Total de reservas.

Ocupação média (%).

Receita média por quarto.

Distribuição de nacionalidade dos hóspedes.

📈 Análise temporal:

Reservas por mês.

Ocupação por estação do ano.

👥 Segmentação de clientes:

Tipo de hóspede (individual, família, empresa).

Percentual de cancelamentos.

📄 Exportação:

Download de relatórios em CSV.

🗃️ Estrutura do Banco de Dados
O banco de dados simulado contém as seguintes tabelas principais:

reservas
Campo	Tipo	Descrição
id_reserva	INTEGER	ID da reserva
data_checkin	DATE	Data de entrada
data_checkout	DATE	Data de saída
id_cliente	INTEGER	FK para tabela clientes
status	TEXT	Status (Confirmada, Cancelada)
receita	DECIMAL	Receita total da reserva

clientes
Campo	Tipo	Descrição
id_cliente	INTEGER	ID do cliente
nome	TEXT	Nome completo
tipo	TEXT	Individual, Família, Empresa
nacionalidade	TEXT	País de origem

quartos
Campo	Tipo	Descrição
id_quarto	INTEGER	ID do quarto
tipo_quarto	TEXT	Standard, Luxo, Suíte etc.
preco_noite	DECIMAL	Preço por noite

🔎 Exemplos de Consultas SQL
Total de reservas:

sql
Copiar
Editar
SELECT COUNT(*) FROM reservas;
Receita média:

sql
Copiar
Editar
SELECT AVG(receita) FROM reservas WHERE status = 'Confirmada';
Reservas por mês:

sql
Copiar
Editar
SELECT strftime('%m', data_checkin) AS mes, COUNT(*) FROM reservas GROUP BY mes;
💻 Tecnologias Utilizadas
Backend: Python (Flask)

Frontend: HTML, CSS, JavaScript (Chart.js)

Banco de Dados: SQLite

Ferramentas: Visual Studio Code, DB Browser

🚦 Como Rodar o Projeto
1️⃣ Clone o repositório:

bash
Copiar
Editar
git clone https://github.com/seuusuario/hotel-insights.git
cd hotel-insights
2️⃣ Instale as dependências (caso use Flask):

bash
Copiar
Editar
pip install flask
3️⃣ Rode o app:

bash
Copiar
Editar
flask run
4️⃣ Acesse no navegador:

cpp
Copiar
Editar
http://127.0.0.1:5000/
🎯 Roadmap
 Estrutura inicial do banco de dados.

 Consultas SQL básicas.

 Montagem do backend (API Flask).

 Dashboard com dados dinâmicos.

 Exportação de relatórios.

 Implementar autenticação de usuários.

✍️ Autora
Adila Zaira 

🌍 Brasil

