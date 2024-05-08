Pré-requisitos
    PHP => 7.4
    Orientado a objetos
    MariaDB/MySQL
    Javascript
    React Native/VueJS/Ionic

Introdução:
    Criar uma base de dados com a seguinte estrutura:

    Tabela: users
    Colunas:
        id 
        name
        phone
        city
        country
        password
        active
        created_at
        updated_at

    Tabela: products
    Colunas: 
        id
        name
        price
        created_at
        updated_at

    Tabela: orders
    Colunas: 
        id
        reference (Referencia da order, deverá ser unica)
        id_user (Deve esta relacionada com a tabela users coluna id)
        created_at
        updated_at

    Tabela: orders_x_products
    Colunas: 
        id
        id_order (Deve esta relacionada com a tabela orders com a coluna id)
        id_product (Deve esta relacionada com a products com a coluna id)
        created_at
        updated_at

    * Para cada produto deve ser criada um registo de subscricao com a mesma order
    Tabela: subscriptions
    Colunas: 
        id
        id_order (Deve esta relacionada com a tabela orders com a coluna id)
        id_product (Deve esta relacionada com a products com a coluna id)
        subscriptions_start (Deverá esta no formato DATETIME)
        subscriptions_end (Deverá esta no formato DATETIME)
        created_at
        updated_at


Deverá criar uma Rest API em PHP que faça autenticacao e crud da respectiva base de dados criada.


Desenvolver uma APP

Autenticão:
    So fará autenticacao se a coluna active for igual a 1.

Dashboard:
    - Na pagina inicial deverá ter todos os produtos adquiridos e sua respectivas informacoes de subscricao:
    start e end.
    - Deverá ter um crud dos dados pessoais (Perfil).
    - Deverá ter no separador um foreach dos produtos e um cor verde quando estiver activo a subscricao e uma cor vermelha quando estiver inativo.
    - Criar função de logout.