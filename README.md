# Style Guide - TCC
## (TypeScript; JavaScript; HTML; CSS)

---

# JavaScript
```


```
# TypeScript
```
function somar(a: number, b: number): number {
  return a + b;
}
```

# HTML
```
<button class="btn">Enviar</button>

<header></header>
<nav></nav>
<main></main>
<section></section>
<footer></footer>
```

# CSS
**ROOT**
```
:root {
  --color-title: #000000;
  --color-text: #F2F2F2;
  --color-navbar: #993030;
  --color-background: #D9C6BA;
}
```

```

```
---

Claro. Abaixo está um prompt completo e estruturado para colar no Claude, pensado para ele atuar como arquiteto + desenvolvedor do projeto, levando em consideração que você vai fornecer posteriormente as telas do Figma.

Projeto: Plataforma Web para Escola Privada de Inglês

Quero que você atue como um desenvolvedor full-stack sênior, arquiteto de software e especialista em UI/UX, responsável por planejar e desenvolver uma plataforma web completa para uma escola privada de inglês.

O projeto deve ser desenvolvido com foco em organização, segurança, responsividade, facilidade de manutenção e fidelidade visual às telas que fornecerei posteriormente pelo Figma.

As telas do Figma devem ser consideradas como a principal referência visual do projeto. Quando eu fornecer imagens/telas do Figma, analise cuidadosamente espaçamentos, proporções, tipografia, componentes, hierarquia visual, bordas, sombras, ícones, botões, menus, cards e demais elementos.

1. Objetivo geral

O sistema será uma plataforma privada para alunos e administradores de uma escola de inglês.

O objetivo principal NÃO é oferecer uma plataforma tradicional de EAD com aulas por vídeo ou exercícios.

A plataforma servirá principalmente para:

Disponibilizar materiais didáticos em PDF;
Exibir o cronograma de aulas de cada aluno;
Informar o conteúdo que será estudado em cada aula;
Permitir que o administrador cadastre e gerencie alunos;
Permitir o acompanhamento de pagamentos;
Permitir a edição do boletim/notas do aluno;
Armazenar informações pessoais dos alunos;
Permitir upload e gerenciamento de materiais;
Permitir que o administrador programe conteúdos e datas de aulas futuras;
Permitir que o aluno consulte suas informações, materiais, boletim e cronograma.

Não haverá:

Videochamadas;
Sistema próprio de videoconferência;
Exercícios interativos;
Sistema de provas online;
Correção automática de exercícios;
Chat entre professor e aluno;
Sistema de aulas por streaming.

O sistema deve ser enxuto e focado nessas funcionalidades.

2. Tecnologias

O frontend deve ser desenvolvido utilizando:

HTML5;
CSS3;
JavaScript.

Não utilize frameworks frontend como React, Vue ou Angular, a menos que eu solicite explicitamente.

O código deve ser organizado de maneira profissional, modular e fácil de compreender.

Caso seja necessário um backend para autenticação, banco de dados, armazenamento dos PDFs e persistência das informações, proponha uma arquitetura adequada e explique claramente a escolha.

O sistema deve separar claramente:

Frontend;
Backend/API, caso utilizado;
Banco de dados;
Armazenamento de arquivos;
Autenticação/autorização.

Não quero uma solução onde dados importantes sejam simplesmente armazenados em variáveis JavaScript ou localStorage como se isso fosse um sistema real de produção.

3. Identidade visual

A identidade visual principal da plataforma será baseada em:

Vermelho;
Branco.

O vermelho deve ser utilizado como cor de destaque da identidade da escola, enquanto o branco deve proporcionar limpeza visual e legibilidade.

Evite criar uma interface excessivamente colorida.

Utilize cores auxiliares apenas quando necessário, por exemplo:

Cinza para textos secundários;
Verde para pagamentos confirmados;
Amarelo para pendências;
Vermelho mais escuro para alertas;
Tons neutros para backgrounds.

A aparência deve transmitir:

Profissionalismo;
Organização;
Confiança;
Modernidade;
Simplicidade;
Sensação de instituição educacional privada.

Quando eu enviar as telas do Figma, priorize a aparência delas em relação a qualquer interpretação sua sobre design.

Não invente componentes que alterem significativamente o layout apresentado.

4. Estrutura de usuários

Existirão dois tipos principais de usuários:

Administrador

O administrador terá acesso ao painel administrativo.

Ele deverá realizar login utilizando:

Username;
Senha.

Após autenticar, terá acesso às funcionalidades administrativas.

Aluno

O aluno também terá uma área própria após realizar login.

O aluno não deve possuir acesso às funcionalidades administrativas.

5. Autenticação e segurança

Implemente uma autenticação adequada.

O sistema deverá possuir controle de permissões baseado em função/role.

Exemplo:

ADMIN
STUDENT


O administrador pode acessar o painel administrativo.

O aluno pode acessar somente sua própria área.

Um aluno NÃO pode:

Visualizar dados de outro aluno;
Alterar seu próprio boletim;
Alterar pagamentos;
Fazer upload de materiais;
Alterar cronogramas;
Alterar informações administrativas.

O administrador poderá visualizar e editar os dados permitidos pelo sistema.

As senhas nunca devem ser armazenadas em texto puro.

Caso exista backend:

Utilize hash seguro de senha;
Faça validação de autenticação no servidor;
Faça autorização no servidor;
Não confie apenas em verificações JavaScript do frontend;
Proteja rotas administrativas;
Valide uploads;
Faça validação dos dados recebidos;
Evite exposição de informações sensíveis.

Explique também como a autenticação deverá funcionar.

6. Painel do administrador

Após realizar login, o administrador deverá acessar um dashboard.

O dashboard deve apresentar uma visão geral da escola.

Sugestões de informações:

Quantidade total de alunos;
Alunos ativos;
Pagamentos pendentes;
Pagamentos confirmados;
Próximas aulas;
Materiais recentemente adicionados;
Alertas importantes.

A estrutura final deve respeitar o Figma quando ele for fornecido.

7. Gerenciamento de alunos

O administrador deverá possuir uma área para cadastro e gerenciamento dos alunos.

Cada aluno poderá possuir informações como:

Dados pessoais
Nome completo;
CPF ou outro identificador, se necessário;
Data de nascimento;
E-mail;
Telefone;
Endereço;
Foto;
Data de cadastro;
Status do aluno.
Dados acadêmicos
Nível de inglês;
Turma, caso aplicável;
Professor responsável, caso aplicável;
Data de início;
Observações;
Progresso;
Informações relevantes.
Dados financeiros
Status do pagamento;
Valor;
Data de vencimento;
Data do pagamento;
Histórico de pagamentos.

Não crie campos desnecessários. A estrutura deve poder ser ajustada posteriormente.

O administrador deve conseguir:

Criar aluno;
Editar aluno;
Visualizar aluno;
Desativar aluno;
Pesquisar aluno;
Filtrar alunos;
Consultar informações do aluno.
8. Boletim

Cada aluno deverá possuir um boletim.

O administrador poderá editar as informações do boletim.

O aluno poderá apenas visualizar.

O boletim pode possuir, por exemplo:

Nome da disciplina/área;
Período;
Nota;
Frequência, caso seja utilizada;
Observações;
Status.

Exemplo:

Grammar       9.0
Vocabulary    8.5
Speaking      9.2
Listening     8.8
Reading       9.0
Writing       8.7


Esses campos são apenas exemplos.

A estrutura deve ser flexível para permitir alterações futuras.

O administrador deve conseguir adicionar, editar e remover informações do boletim.

O aluno deve visualizar uma versão somente leitura.

9. Cronograma de aulas

Essa será uma das funcionalidades mais importantes.

O administrador deverá conseguir criar o cronograma individual de cada aluno.

Cada evento/aula deverá poder conter:

Data;
Horário;
Conteúdo da aula;
Título;
Descrição;
Status;
Observações, se necessário.

Exemplo:

12/09/2026
19:00

Conteúdo:
Present Perfect

Descrição:
Introdução ao Present Perfect, utilização em frases afirmativas,
negativas e interrogativas.


O administrador deverá conseguir:

Adicionar aula;
Editar aula;
Excluir aula;
Alterar data;
Alterar horário;
Alterar conteúdo;
Adicionar conteúdos futuros;
Visualizar aulas passadas;
Visualizar próximas aulas.

O aluno deverá visualizar seu próprio cronograma.

O aluno NÃO poderá editar o cronograma.

10. Materiais em PDF

O administrador deverá possuir uma área para gerenciamento dos materiais.

Ele poderá:

Fazer upload de PDFs;
Adicionar título;
Adicionar descrição;
Definir categoria;
Definir para qual aluno ou grupo o material será disponibilizado;
Excluir material;
Substituir material;
Visualizar materiais cadastrados.

A página do aluno deverá mostrar os materiais aos quais ele possui acesso.

O aluno deverá conseguir:

Visualizar informações do material;
Abrir o PDF;
Fazer download, caso essa funcionalidade esteja habilitada.

Importante:

Os arquivos não devem ser simplesmente expostos em uma pasta pública sem qualquer controle.

Analise uma estratégia adequada para armazenamento e autorização dos arquivos.

Também implemente validações para upload:

Permitir somente formatos definidos;
Verificar tamanho máximo;
Validar extensão e MIME type;
Gerar nomes seguros para arquivos;
Evitar problemas de path traversal;
Não confiar no nome original do arquivo.
11. Área do aluno

Depois do login, o aluno deverá acessar um dashboard próprio.

A página inicial deve apresentar informações relevantes de maneira simples.

Por exemplo:

Próxima aula;
Data e horário;
Próximo conteúdo;
Últimos materiais adicionados;
Resumo do boletim;
Status do pagamento, se essa informação for disponibilizada ao aluno.

O aluno deverá ter acesso a páginas como:

Dashboard
Cronograma
Materiais
Boletim
Meu perfil


A estrutura exata deverá ser adaptada às telas do Figma.

12. Página de cronograma do aluno

A página deverá apresentar suas aulas de maneira organizada.

Pode utilizar:

Lista;
Cards;
Calendário;
Timeline;

ou uma combinação dessas opções, dependendo do Figma.

Cada aula deve apresentar claramente:

Data;
Horário;
Conteúdo;
Descrição;
Status.

O usuário deve conseguir identificar facilmente:

Aulas futuras;
Aulas realizadas;
Próxima aula.
13. Página de materiais

O aluno deverá visualizar os materiais disponibilizados pelo administrador.

Cada material pode apresentar:

Nome;
Categoria;
Data de disponibilização;
Descrição;
Ícone de PDF;
Botão para abrir;
Botão para download, caso permitido.

A interface deve ser simples e organizada.

14. Página de boletim

O aluno deverá conseguir consultar seu boletim.

A página deverá possuir visualização clara das notas.

Pode utilizar:

Tabela;
Cards;
Indicadores;
Média geral;

desde que esteja de acordo com o Figma.

O aluno não deverá conseguir editar essas informações.

15. Perfil do aluno

O aluno poderá visualizar suas informações pessoais.

Dependendo do layout do Figma, pode haver:

Nome;
Foto;
E-mail;
Telefone;
Data de nascimento;
Nível;
Informações acadêmicas.

Caso o aluno possa editar alguma informação, defina explicitamente quais campos podem ser alterados.

Não permita que informações críticas sejam alteradas sem validação.

16. Pagamentos

O administrador deverá possuir controle do status financeiro dos alunos.

Não será necessário inicialmente integrar um gateway de pagamento.

O sistema deverá permitir registrar informações como:

Aluno
Valor
Vencimento
Data do pagamento
Status
Observação


Status possíveis:

PENDING
PAID
OVERDUE
CANCELLED


O administrador deverá conseguir confirmar manualmente um pagamento.

Se o aluno tiver acesso ao status financeiro, ele deverá ser somente leitura.

17. Banco de dados

Projete uma estrutura de banco de dados adequada.

Sugira as principais entidades, por exemplo:

users
students
profiles
grades
grade_items
materials
lessons
payments


A estrutura final deve ser normalizada e evitar duplicação desnecessária.

Explique os relacionamentos.

Por exemplo:

User
  ↓
Student Profile
  ↓
Lessons
  ↓
Materials
  ↓
Grades
  ↓
Payments


Se utilizar banco relacional, apresente o modelo das tabelas e seus relacionamentos.

18. API

Caso seja utilizado backend, organize a API de maneira RESTful.

Exemplos:

POST   /api/auth/login

GET    /api/students
POST   /api/students
GET    /api/students/:id
PUT    /api/students/:id
DELETE /api/students/:id

GET    /api/students/:id/schedule
POST   /api/students/:id/schedule
PUT    /api/schedule/:id
DELETE /api/schedule/:id

GET    /api/materials
POST   /api/materials
DELETE /api/materials/:id

GET    /api/students/:id/grades
PUT    /api/students/:id/grades

GET    /api/students/:id/payments
POST   /api/payments
PUT    /api/payments/:id


Não precisa seguir exatamente essa estrutura se você identificar uma arquitetura melhor.

19. Frontend

Organize o frontend de forma profissional.

Uma estrutura possível:

/frontend
    /pages
        login.html
        admin-dashboard.html
        admin-students.html
        admin-student.html
        admin-materials.html
        admin-schedule.html
        student-dashboard.html
        student-schedule.html
        student-materials.html
        student-grades.html
        student-profile.html

    /css
        reset.css
        variables.css
        global.css
        components.css
        layout.css
        pages/

    /js
        api.js
        auth.js
        utils.js
        admin/
        student/

    /assets
        /images
        /icons


Essa é apenas uma sugestão.

Se você identificar uma estrutura melhor, utilize-a e explique o motivo.

Evite colocar centenas de linhas de CSS e JavaScript em um único arquivo.

20. Responsividade

O sistema deverá funcionar adequadamente em:

Desktop;
Notebook;
Tablet;
Smartphone.

Priorize principalmente:

Menu responsivo;
Tabelas adaptáveis;
Cards;
Formulários;
Dashboard;
Cronograma;
Visualização de PDFs.

Não simplesmente diminua elementos para mobile.

Reorganize os componentes quando necessário.

21. Acessibilidade

Implemente boas práticas de acessibilidade:

HTML semântico;
Labels nos inputs;
Contraste adequado;
Foco visível;
Navegação por teclado;
Alt text em imagens;
Botões semanticamente corretos;
Mensagens de erro compreensíveis.

Não utilize div como botão quando um elemento <button> for apropriado.

22. UX

A plataforma deve ser simples de utilizar.

Evite:

Interfaces excessivamente complexas;
Menus desnecessários;
Informações redundantes;
Animações exageradas;
Pop-ups sem necessidade.

Utilize feedback visual para ações importantes:

Sucesso;
Erro;
Carregamento;
Confirmação;
Exclusão.

Exemplo:

Material enviado com sucesso.


ou:

Não foi possível salvar as alterações.
Tente novamente.

23. Estados de carregamento e erro

Todas as operações que dependem do backend devem possuir estados adequados.

Por exemplo:

Carregando alunos...


Caso não existam dados:

Nenhum aluno cadastrado.


Caso ocorra erro:

Não foi possível carregar os dados.


Não deixe a interface simplesmente vazia quando uma requisição falhar.

24. Validação de formulários

Todos os formulários devem possuir validação.

Exemplos:

Campos obrigatórios;
E-mail válido;
Senha com requisitos mínimos;
Datas válidas;
Valores monetários válidos;
Arquivos permitidos;
Limite de tamanho;
Horários válidos.

A validação deve existir no frontend para melhorar a experiência, mas também no backend para segurança.

25. Código

Quero código:

Limpo;
Organizado;
Legível;
Modular;
Comentado somente quando necessário;
Sem duplicações desnecessárias;
Sem código morto;
Sem dados falsos escondidos no sistema final.

Evite:

// TODO
// implementar depois


quando a funcionalidade já deveria estar implementada.

Não utilize soluções improvisadas apenas para "fazer parecer que funciona".

Se alguma parte precisar de uma implementação provisória, deixe isso explicitamente documentado.

26. Dados fictícios

Durante o desenvolvimento, você pode utilizar dados fictícios para demonstrar o funcionamento da interface.

Porém, diferencie claramente:

MOCK DATA


de dados reais.

Não deixe dados fictícios misturados com a arquitetura de produção.

27. Figma

Eu fornecerei posteriormente as telas desenvolvidas no Figma.

Quando eu enviar uma tela:

Analise visualmente a tela;
Identifique a estrutura;
Identifique componentes reutilizáveis;
Identifique cores;
Identifique tipografia;
Identifique espaçamentos;
Identifique dimensões aproximadas;
Identifique estados dos componentes;
Reproduza o layout em HTML/CSS;
Adapte para responsividade sem destruir o design original.

Não substitua o design por um dashboard genérico.

O resultado deve parecer uma implementação real das telas do Figma.

Se alguma informação do Figma estiver ambígua, faça uma suposição razoável e informe qual foi a decisão tomada.

28. Componentização

Mesmo utilizando HTML/CSS/JavaScript puro, crie componentes reutilizáveis.

Exemplos:

Sidebar;
Header;
Button;
Modal;
Input;
Select;
Card;
Table;
Badge;
Toast;
Empty State;
Loading State;
Confirmation Dialog.

Evite copiar e colar o mesmo HTML em dezenas de páginas.

29. Dashboard administrativo

O administrador deverá conseguir navegar facilmente entre:

Dashboard
Alunos
Pagamentos
Materiais
Cronogramas
Boletins
Configurações
Sair


A estrutura final deve seguir o Figma.

30. Dashboard do aluno

O aluno deverá possuir uma navegação simplificada:

Início
Cronograma
Materiais
Boletim
Meu perfil
Sair


Novamente, adapte à interface do Figma.

31. Controle de acesso

Implemente proteção de rotas.

Exemplo:

/admin/*


Somente ADMIN.

/student/*


Somente STUDENT.

Além disso, um aluno autenticado não deve conseguir simplesmente alterar a URL para acessar informações administrativas.

A autorização deve ser validada também no backend.

32. Privacidade

O sistema manipulará dados pessoais de alunos.

Portanto, trate os dados com cuidado.

Não exponha informações de um aluno para outro.

Evite retornar dados desnecessários nas APIs.

Retorne somente os campos necessários para cada operação.

33. Preparação para produção

O código deve ser estruturado pensando em uma aplicação que futuramente poderá ser publicada na internet.

Considere:

Variáveis de ambiente;
Configuração de produção;
Segurança;
Logs;
Tratamento de erros;
CORS quando necessário;
HTTPS em produção;
Proteção de endpoints;
Backup do banco;
Armazenamento seguro dos PDFs.

Não coloque secrets, senhas ou chaves diretamente no código.

34. O que NÃO fazer

Não faça:

Um simples HTML estático fingindo ser um sistema completo;
Senhas armazenadas em JavaScript;
Dados sensíveis em localStorage sem necessidade;
Autenticação apenas no frontend;
PDFs públicos sem controle de acesso;
Interface genérica que ignore o Figma;
Código inteiro em um único arquivo;
Dados de todos os alunos enviados para qualquer usuário;
Permissão para aluno editar informações administrativas;
Upload sem validação;
SQL inseguro;
Senhas em texto puro;
Código excessivamente complexo sem necessidade.
35. Processo de desenvolvimento

Antes de começar a escrever todo o código, faça primeiro uma análise do projeto.

Apresente:

Etapa 1 — Arquitetura

Explique:

Stack recomendada;
Estrutura de pastas;
Banco de dados;
Backend;
Frontend;
Autenticação;
Armazenamento de PDFs.
Etapa 2 — Modelagem

Apresente:

Entidades;
Tabelas;
Campos;
Relacionamentos;
Regras de negócio.
Etapa 3 — Fluxos

Descreva os fluxos:

Login administrador
↓
Dashboard
↓
Gerenciar alunos
↓
Selecionar aluno
↓
Editar boletim / cronograma / pagamentos


E:

Login aluno
↓
Dashboard
↓
Cronograma
↓
Materiais
↓
Boletim
↓
Perfil

Etapa 4 — Interface

Quando eu fornecer o Figma, analise cada tela e converta para HTML/CSS/JavaScript.

Etapa 5 — Implementação

Implemente o projeto por etapas.

Não tente criar tudo de uma vez se isso comprometer a qualidade.

Etapa 6 — Testes

Depois da implementação, verifique:

Login;
Permissões;
Cadastro;
Edição;
Exclusão;
Upload;
Cronograma;
Boletim;
Pagamentos;
Responsividade;
Erros;
Segurança.
36. Como quero que você responda

Quero que você seja crítico durante o desenvolvimento.

Se alguma decisão minha não for adequada tecnicamente, explique o problema e proponha uma alternativa.

Não concorde automaticamente comigo.

Quando existir mais de uma solução possível, compare brevemente as alternativas e escolha a mais adequada.

Priorize:

Segurança;
Manutenibilidade;
Simplicidade;
Experiência do usuário;
Fidelidade ao Figma;
Performance.
37. Regra importante sobre o Figma

Quando eu enviar as imagens das telas, não comece imediatamente criando um design diferente.

Primeiro:

Observe a tela;
Identifique o layout;
Identifique o grid;
Identifique os componentes;
Identifique as cores;
Identifique a hierarquia;
Identifique os padrões repetidos.

Depois explique brevemente como pretende reproduzi-la.

Só então implemente.

Se eu enviar várias telas, procure padrões para criar componentes compartilhados.

38. Resultado esperado

Ao final, quero ter uma plataforma web funcional para uma escola privada de inglês, contendo:

Administrador
Login;
Dashboard;
Cadastro de alunos;
Consulta de alunos;
Edição de alunos;
Controle de pagamentos;
Edição de boletim;
Gerenciamento de materiais;
Upload de PDFs;
Gerenciamento de cronogramas;
Cadastro de aulas futuras;
Cadastro de conteúdos;
Edição e exclusão de aulas.
Aluno
Login;
Dashboard;
Visualização do cronograma;
Visualização dos conteúdos das aulas;
Acesso aos materiais PDF;
Visualização do boletim;
Visualização das informações pessoais;
Visualização do status financeiro, caso definido no projeto.
39. Primeira tarefa

Neste momento, NÃO comece criando todas as páginas.

Primeiro faça uma análise técnica completa do projeto.

Quero que você me entregue:

Arquitetura recomendada;
Stack completa;
Estrutura de pastas;
Modelo do banco de dados;
Entidades e relacionamentos;
Fluxo de autenticação;
Fluxo do administrador;
Fluxo do aluno;
Estrutura das APIs;
Estratégia para armazenamento dos PDFs;
Estratégia de segurança;
Estratégia de responsividade;
Estratégia de componentização;
Lista de páginas necessárias;
Ordem recomendada de implementação.

Depois disso, aguardará as telas do Figma que enviarei.

Não implemente as telas antes de analisar o Figma.

Quando eu enviar as telas, use-as como referência visual principal e implemente o frontend em HTML, CSS e JavaScript mantendo a identidade visual em vermelho e branco.

Esse prompt já deixa o Claude com contexto de produto, arquitetura, regras de acesso, segurança, banco de dados, UX e fluxo de desenvolvimento, em vez de simplesmente pedir para ele "fazer um site".

Se você quiser, também posso montar uma versão ainda mais técnica, já direcionada para uma stack específica (por exemplo HTML/CSS/JS + Node.js + Express + PostgreSQL), incluindo a estrutura das tabelas SQL, endpoints e organização dos arquivos para o Claude começar a programar diretamente.

