README – Implantação Completa do Sistema Fuji, de Gestão para Academias de Lutas

INTRODUÇÃO

Este documento descreve detalhadamente como implantar, configurar
e recriar do zero o Sistema de Gestão para Academias de Lutas.
Ele serve como guia definitivo para restaurar o projeto em um
ambiente novo, realizar personalizações e entender toda a
estrutura necessária para execução em produção.

O sistema atual é um FRONT-END ESTÁTICO composto por:
- Arquivos HTML
- Arquivos CSS
- Imagens
Não há banco de dados, backend, autenticação real ou APIs.

O objetivo deste arquivo é garantir que QUALQUER pessoa 
consiga reconstruir o projeto exatamente como está,
mesmo sem conhecimento prévio do código.

1. OBJETIVO DO SISTEMA

Este sistema é um SaaS (Software como Serviço) destinado a
múltiplas academias de lutas. NÃO é um site para uma única
academia, mas sim um produto que pode ser contratado por várias
academias e personalizado com:
- Nome da academia
- Modalidades oferecidas
- Logotipo
- Textos institucionais

O sistema permite:
- Exibição de páginas institucionais
- Exibição de modalidades (Boxe, Jiu-Jitsu, Muay Thai, etc.)
- Exibição de grade resumida de treinos
- Painel visual do aluno (simulado)

2. ESTRUTURA DE DIRETÓRIOS

No projeto, a estrutura deve aparecer assim:

/
|-- index.html               (Página inicial / institucional)
|-- aluno.html               (Painel do aluno – versão estática)
|-- boxe.html                (Modalidade: Boxe)
|-- capoeira.html            (Modalidade: Capoeira)
|-- jiujitsu.html            (Modalidade: Jiu-Jitsu)
|-- kickboxing.html          (Modalidade: Kickboxing)
|-- mma.html                 (Modalidade: MMA)
|-- muaythai.html            (Modalidade: Muay Thai)
|-- style.css                (Estilos da página principal e modalidades)
|-- stylealuno.css
|-- img/
      |-- logotipo.png ou similar
      |-- imagens ilustrativas

3. PRÉ-REQUISITOS

PARA RODAR LOCALMENTE:
- Navegador atualizado (Chrome, Edge, Firefox)

PARA RODAR EM PRODUÇÃO:
- QUALQUER servidor que aceite arquivos estáticos:
  * Apache
  * Nginx
  * Hostinger / Locaweb
  * GitHub Pages
  * Netlify
  * Vercel
Nenhuma linguagem de backend é necessária.

4. COMO RECONSTRUIR O PROJETO DO ZERO

Se tudo for perdido, siga estes passos para recriar:

1. Criar os arquivos HTML listados na estrutura.
2. Criar o arquivo style.css com estilos gerais.
3. Criar stylealuno.css
4. Criar a pasta img/ e colocar as imagens usadas.
5. Incluir nos HTML:
   - Header com navegação
   - Sessões internas
   - Links para modalidades
   - Links corretos para CSS e imagens
6. Para o painel do aluno (aluno.html):
   - Criar estrutura de cards
   - Importar o CSS stylealuno.css
   - Importar os ícones Lucide (online)
7. Testar navegabilidade em:
   - index.html
   - aluno.html
   - páginas de modalidades


5. IMPLANTAÇÃO LOCAL (PASSO A PASSO)

PASSO 1 — Desenvolver o Código
Crie uma pasta e coloque todo o conteúdo dentro dela.

Edite aluno.html e garanta:
<link rel="stylesheet" href="stylealuno.css">

PASSO 3 — Testar localmente
Basta clicar duas vezes em index.html.

6. IMPLANTAÇÃO EM PRODUÇÃO

6.1 HOSPEDAGEM COMPARTILHADA

1. Acesse o gerenciador de arquivos.
2. Vá para public_html ou www.
3. Envie TODOS os arquivos do sistema.
4. Mantenha a estrutura original.
5. Acesse:
https://seudominio.com/


6.2 GITHUB PAGES

1. Criar repositório.
2. Fazer upload dos arquivos.
3. Ativar Pages em "Settings → Pages".
4. Acessar URL gerada.


7. PERSONALIZAÇÃO PARA CADA ACADEMIA


7.1 Trocar logotipo:
Substituir arquivos da pasta img/ e ajustar src nos HTML.

7.2 Ajustar nome da academia:
Modificar textos no index.html.

7.3 Alterar modalidades:
Adicionar arquivos HTML duplicando qualquer modalidade existente.

7.4 Alterar cores e estilos:
Editar style.css e stylealuno.css.

8. PONTOS DE ATENÇÃO

- O painel do aluno NÃO tem backend.
- Nada é salvo — tudo é visual.
- Para tornar o sistema real seria preciso:
  * backend (Node, PHP, Python, etc.)
  * banco de dados
  * autenticação
  * painel administrativo

9. CONCLUSÃO

Seguindo este guia, qualquer desenvolvedor ou avaliador poderá:
- Restaurar o projeto do zero
- Implantar localmente ou em produção
- Personalizar para academias diferentes
- Compreender toda a arquitetura do sistema

