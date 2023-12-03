# resumoApiREST

# API REST e RESTFull <h1>

## API REST (Representational State Transfer) <h2>
É um estilo arquitetural para sistemas distribuídos, focado na interação entre componentes, e é uma abordagem eficaz para criar serviços web interoperáveis e escaláveis, seguindo princípios simples e padronizados.

**Princípios fundamentais**
1. Arquitetura Cliente-Servidor: Separação clara entre a lógica do cliente e do servidor.
2. Stateless (Sem Estado): Cada requisição do cliente contém toda a informação necessária para entender e processar a requisição.
3. Cache: Utilização de cache para melhorar a eficiência e escalabilidade.
4. Interface Uniforme: Recursos são manipulados de maneira uniforme através de identificadores e representações.

**Elementos-Chave**
1. Recurso (Resource): Entidade ou conceito fundamental, acessível via URI.
2. Representação: A forma como um recurso é apresentado (JSON, XML, etc.).
3. Métodos HTTP: Utilização de métodos padrão (GET, POST, PUT, DELETE) para operações em recursos.

## RESTFull <h2>
Refere-se à implementação dos princípios REST em um sistema, enfatiza a simplicidade, a escalabilidade e a interoperabilidade, proporcionando uma abordagem eficaz para o desenvolvimento de serviços web.

**Princípios fundamentais**
1. Recursos Nomenclaturados: Uso de URIs para identificar recursos de forma significativa e hierárquica.
3. Representações: Utilização de formatos como JSON ou XML para representar dados.
4. Comunicação Stateless: Cada requisição do cliente contém toda a informação necessária, sem dependências de estados anteriores.

**Elementos-Chave**
1. Endpoints Claros: Cada recurso possui um endpoint único e bem definido.
2. Métodos HTTP Semânticos: Uso apropriado dos métodos HTTP (GET, POST, PUT, DELETE) para operações específicas.
3. HATEOAS (Hypermedia As The Engine Of Application State): Inclusão de links em respostas para guiar a navegação do cliente pela aplicação.
 
# Diferenças entre REST e RESTFull <h1>
REST (Representational State Transfer) e RESTFull são termos frequentemente utilizados em contextos de desenvolvimento de APIs, mas possuem distinções sutis.

**Principais Distinções**
* Abstrato vs. Concreto: REST é um conjunto de princípios abstratos, enquanto RESTFull é a aplicação prática desses princípios em um sistema específico.
* Flexibilidade vs. Padronização: REST permite mais flexibilidade na implementação, enquanto RESTFull busca padronização e boas práticas.



# HTTP verbs <h1>
São fundamentais na comunicação entre clientes e servidores por meio do protocolo HTTP. Cada verbo representa uma ação específica a ser realizada sobre um recurso identificado pela URI.

**Principais HTTP Verbs**
1. GET
Descrição: Os clientes usam GET para acessar recursos localizados no URL especificado no servidor. Eles podem armazenar em cache solicitações GET e enviar parâmetros na solicitação da API RESTful para instruir o servidor a filtrar dados antes de enviar.
Exemplo:
Esta é uma linha que contém um ˋcódigoˋ.
 ˋˋˋ
 GET /api/users/123
ˋˋˋ
2. POST
Descrição: Os clientes usam POST para enviar dados ao servidor. Eles incluem a representação de dados com a solicitação. Se enviarem a mesma solicitação POST várias vezes, criarão o mesmo recurso várias vezes.
Esta é uma linha que contém um ˋcódigoˋ.
 ˋˋˋ
 POST /api/users
ˋˋˋ
3. PUT
Descrição: Os clientes usam PUT para atualizar recursos existentes no servidor. Ao contrário do POST, o envio da mesma solicitação PUT várias vezes em um serviço da Web RESTful tem o mesmo resultado.
Exemplo:
Esta é uma linha que contém um ˋcódigoˋ.
 ˋˋˋ
 PUT /api/users/123
ˋˋˋ
4. DELETE
Descrição: Os clientes usam a solicitação DELETE para remover o recurso. Uma solicitação DELETE pode alterar o estado do servidor. No entanto, se o usuário não tiver a autenticação apropriada, a solicitação falhará.
Exemplo:
Esta é uma linha que contém um ˋcódigoˋ.
 ˋˋˋ
 DELETE /api/users/123
ˋˋˋ
5. PATCH
Descrição: Atualiza parcialmente um recurso existente.
Exemplo:
Esta é uma linha que contém um ˋcódigoˋ.
 ˋˋˋ
PATCH /api/users/123
ˋˋˋ
6. HEAD
Descrição: Semelhante ao GET, mas sem o corpo da resposta, útil para obter metadados.
Exemplo:
Esta é uma linha que contém um ˋcódigoˋ.
 ˋˋˋ
HEAD /api/users/123
ˋˋˋ
7. OPTIONS
Descrição: Retorna os métodos HTTP suportados em um determinado recurso.
Exemplo:
Esta é uma linha que contém um ˋcódigoˋ.
 ˋˋˋ
OPTIONS /api/users
ˋˋˋ
8. TRACE
Descrição: Usado para diagnosticar a rota entre o cliente e o servidor.
Exemplo:
Esta é uma linha que contém um ˋcódigoˋ.
 ˋˋˋ
TRACE /path/to/resource
ˋˋˋ
9. CONNECT
Descrição: Usado para indicar ao servidor que o cliente deseja estabelecer uma conexão com recursos identificados no URI.
Exemplo:
Esta é uma linha que contém um ˋcódigoˋ.
 ˋˋˋ
CONNECT server:80
ˋˋˋ


# HTTP Status Code <h1>
Os códigos de status HTTP são retornados como parte das respostas do servidor para indicar o resultado da solicitação feita pelo cliente. Cada código de status é composto por três dígitos e está agrupado em classes que indicam a natureza da resposta.

Classes Principais
1. 1xx - Informativos
* 100 Continue: O servidor recebeu a solicitação inicial e o cliente pode continuar com a solicitação.
   
2. 2xx - Sucesso
* 200 OK: A solicitação foi bem-sucedida.
* 201 Created: A solicitação foi bem-sucedida, e um novo recurso foi criado como resultado.
* 204 No Content: A solicitação foi bem-sucedida, mas não há conteúdo para ser retornado.

3. 3xx - Redirecionamento
* 301 Moved Permanently: O recurso solicitado foi movido permanentemente para uma nova localização.
* 302 Found (ou 303 See Other): O recurso foi temporariamente movido para uma nova localização.

4. 4xx - Erro do Cliente
* 400 Bad Request: A solicitação do cliente é inválida ou malformada.
* 401 Unauthorized: O cliente deve se autenticar para obter a resposta solicitada.
* 403 Forbidden: O cliente não tem permissões suficientes para acessar o recurso.
* 404 Not Found: O recurso solicitado não foi encontrado no servidor.

5. 5xx - Erro do Servidor
* 500 Internal Server Error: O servidor encontrou uma situação inesperada que impediu o processamento da solicitação.
* 502 Bad Gateway: O servidor, enquanto atuando como gateway ou proxy, recebeu uma resposta inválida do servidor upstream.
* 503 Service Unavailable: O servidor não está pronto para manipular a solicitação. Geralmente, está temporariamente fora de serviço.   

Autor do resumo: Gabriely Xavier - 01570523

