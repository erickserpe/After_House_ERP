# After House ERP 🍹

**Sistema de gestão inteligente para open bar, com foco em planejamento de eventos, controle de custos e gerenciamento de insumos.**

O **After House ERP** foi desenvolvido para simplificar a vida de organizadores de eventos e donos de bar, oferecendo um controle completo sobre todos os aspectos do serviço de open bar. Desde o cadastro de produtos e fornecedores até a simulação detalhada de eventos, o sistema automatiza cálculos e otimiza a gestão de compras.

O projeto utiliza uma interface moderna com efeito "glassmorphism" para uma experiência de usuário agradável e intuitiva.

---

## ✨ Funcionalidades Principais

* **👤 Gestão de Usuários:** Cadastro, login seguro com senhas criptografadas (`password_hash`) e funcionalidade de "mudar senha".
* **📈 Dashboard de Performance:** Um painel visual com os principais indicadores (KPIs) de eventos, análise de custos, produtos mais usados e um funil de status de eventos.
* **📦 Gestão de Insumos:**
    * **Produtos:** Cadastro de todos os insumos (bebidas, frutas, etc.) com preço de compra, unidade de medida e fornecedor associado.
    * **Fornecedores:** Cadastro de contatos de fornecedores.
    * **Estoque:** Controle de estoque fácil com funcionalidade para dar entrada em novas compras.
* **🍸 Receitas Inteligentes:** Crie receitas (drinks) associando produtos como ingredientes. O sistema calcula o custo exato de cada receita.
* **📊 Simulador de Eventos:** A ferramenta central do sistema.
    * Crie um evento com base no número de pessoas e nas receitas selecionadas.
    * O sistema gera uma **lista de compras inteligente**, mostrando exatamente o que precisa ser comprado ao comparar o necessário com o estoque atual.
    * Salva o evento em modo "Planejamento" para gestão futura.
* **🎉 Gestão de Eventos Completa:**
    * Acompanhe o status de todos os eventos (Planejamento, Confirmado, Realizado, Cancelado).
    * Edite o cardápio a qualquer momento, e o sistema recalcula a lista de compras automaticamente.
    * Funcionalidade de "Realizar Evento" que dá baixa nos insumos utilizados diretamente do estoque.

---

## 🛠️ Tecnologias Utilizadas

* **Backend:** PHP 8+
* **Banco de Dados:** MySQL
* **Frontend:**
    * HTML5 e CSS3 (com Variáveis)
    * JavaScript (Vanilla JS para interatividade)
    * Bootstrap 5 (para a estrutura responsiva e componentes)
    * Chart.js (para os gráficos do dashboard)

---

## 🚀 Instalação e Configuração Local

Siga os passos para rodar o projeto em um ambiente de desenvolvimento (XAMPP, WAMP, etc.).

### Pré-requisitos
* Servidor web local com PHP 8 ou superior.
* Servidor de banco de dados MySQL ou MariaDB.

### Passos

1.  **Clone o Repositório**
    ```bash
    git clone [https://github.com/seu-usuario/after-house-erp.git](https://github.com/seu-usuario/after-house-erp.git)
    cd after-house-erp
    ```

2.  **Banco de Dados**
    * Crie um novo banco de dados no seu servidor MySQL (ex: `after_house`).
    * Importe o arquivo `database.sql` que está na raiz do projeto. Ele criará todas as tabelas necessárias e um usuário administrador padrão.

3.  **Configuração da Conexão**
    * Renomeie o arquivo `includes/db.example.php` para `includes/db.php`.
    * Abra o arquivo `includes/db.php` e altere as credenciais (`$host`, `$user`, `$password`, `$dbname`) para corresponder às do seu ambiente local.
        ```php
        <?php
        $host = 'localhost';
        $user = 'root';
        $password = ''; // ou sua senha do root
        $dbname = 'after_house';
        
        // ... resto do código
        ```

4.  **Acesse o Sistema**
    * Abra o seu navegador e acesse o diretório do projeto (ex: `http://localhost/after-house-erp`).
    * Use as credenciais de administrador para o primeiro acesso:
        * **Email:** `admin@afterhouse.com`
        * **Senha:** `admin123`
