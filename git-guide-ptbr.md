**[PT-BR]**
## **O que é e para que serve o Git e GitHub?**

**Git** é um sistema de controle de versão, o que significa que ele gerencia as alterações em projetos de software ao longo do tempo. Ele permite que várias pessoas trabalhem em um projeto simultaneamente, rastreia as mudanças feitas e facilita a colaboração.

**GitHub** ,por outro lado, é uma plataforma de hospedagem de código que utiliza o Git. É como uma rede social para desenvolvedores, onde eles podem armazenar, compartilhar e colaborar em projetos usando o Git. O GitHub fornece uma interface web amigável para trabalhar com repositórios Git, tornando mais fácil para equipes de desenvolvimento colaborarem em projetos de software.

Resumindo, Git é a tecnologia subjacente que gerencia as versões de um projeto, e o GitHub é uma plataforma que usa o Git para facilitar a colaboração e o gerenciamento de código-fonte.

---

## ******************************Como baixar e instalar o Git.******************************

1. **Baixe o Git:**
    - Vá para o site oficial do Git em [git-scm.com](https://git-scm.com/).
    - Clique no botão de download para o seu sistema operacional (Windows, macOS, Linux, etc.).
2. **Instale o Git:**
    - No Windows, execute o instalador baixado e siga as instruções padrão.
    - No macOS, você pode usar o Homebrew ou o instalador gráfico.
    - No Linux, use o gerenciador de pacotes da sua distribuição.
    
    ---
    

## Como c**onfigurar o Git.**

1. **Abra o Terminal:**
    - Isso é onde você irá interagir com o Git
2. **Configure seu nome de usuário :**
    
    ```bash
    git config --global user.name "Seu Nome"
    ```
    
3. **Configure seu endereço de e-mail:**
    
    ```bash
    git config --global user.email "seu.email@example.com"
    ```
    

### **Verificar Configurações:**

Para verificar se as configurações foram feitas corretamente, digite:

```bash
git config --global --list
```

Isso deverá exibir suas configurações globais.

---

## **Repositório local e remoto.**

### **Repositório Local:**

- É a versão do seu projeto que está armazenada no seu computador. Você interage diretamente com esse repositório, fazendo alterações, commits, etc.

### **Repositório Remoto:**

- É a versão do seu projeto que está hospedada em um servidor remoto, como o GitHub. Ele é usado para colaboração e compartilhamento. Você envia suas alterações do repositório local para o remoto.

---

## Comandos do Git e GitHub.

### Comandos Git:

**`git init`**: Este comando é usado para iniciar um novo repositório Git. Quando você cria um novo projeto, você pode executar **`git init`** no diretório do projeto para começar a rastrear as alterações.

---

**`git clone`**: Usado para clonar (copiar) um repositório existente. Você fornece a URL do repositório que deseja clonar **`git clone url`**, e o Git cria uma cópia local completa no seu computador.

---

**`git add`**: Adiciona mudanças ao próximo commit. Pode ser um arquivo específico (**`git add nome-do-arquivo`**) ou todas as alterações no diretório (**`git add .`**).

---

**`git commit`**: Confirma as alterações que foram adicionadas com **`git add`**. Cada commit tem uma mensagem que descreve as alterações feitas, da seguinte forma `git commit -m`.

---

**`git diff`**: Mostra as diferenças entre o seu diretório de trabalho atual e o último commit.

---

**`git rm`**: Remove arquivos do controle de versão. Também remove os arquivos fisicamente do seu diretório de trabalho.

---

**`git status`**: Mostra o estado atual do seu repositório. Indica quais arquivos foram modificados, adicionados ou estão pendentes para commit.

---

**`git log`**: Exibe o histórico de commits, mostrando quem fez quais alterações e quando.

---

**`git restore`**: Desfaz alterações no diretório de trabalho. Pode ser usado para desfazer alterações específicas ou até mesmo para restaurar um arquivo excluído.

---

**`git branch`**: Lista as branches existentes no seu repositório.

---

**`git branch nova-branch`**   : cria uma nova branch no repositório atual.

---

**`git checkout`**  ou  **`git switch`**: Muda para uma branch específica. Também pode ser usado para criar uma nova branch **`git checkout -b nova-branch`**  ou  **`git switch -c nova-branch`.**

---

**`git merge`**: Combina as alterações de uma branch em outra. Por exemplo, para mesclar o trabalho de uma feature branch de volta para a branch principal.

---

**`git fetch`**: Busca as alterações do repositório remoto, mas não as mescla no seu diretório de trabalho.

---

**`git pull`**: Busca as alterações do repositório remoto e as mescla automaticamente no seu diretório de trabalho.

---

**`git push`**: Envia as alterações locais para o repositório remoto. Útil quando você quer compartilhar seu trabalho ou fazer backup das alterações online.

---

### Comandos GitHub:

**`git remote add origin <URL>`**: Conecta o repositório local a um repositório remoto no GitHub.

---

**`git push -u origin <branch>`**: Define a branch remota padrão.

---

**Pull Request (PR)**: Usado para propor alterações e iniciar uma discussão antes de mesclá-las.

---

**Issues**: Rastreia tarefas, melhorias ou bugs.

---

**Fork**: Cria uma cópia independente de um repositório para que você possa contribuir sem afetar o original.

---

**Clone ou download**: Fornece a URL que você pode usar com **`git clone`**.

---

**Settings**: Configurações do repositório, onde você pode gerenciar colaboradores, acessos e outras configurações.

---

# Padrões de commits 📜

De acordo com a documentação do **[Conventional Commits](https://www.conventionalcommits.org/pt-br)**, commits semânticos são uma convenção simples para ser utilizada nas mensagens de commit. Essa convenção define um conjunto de regras para criar um histórico de commit explícito, o que facilita a criação de ferramentas automatizadas.

Esses commits auxiliarão você e sua equipe a entenderem de forma facilitada quais alterações foram realizadas no trecho de código que foi commitado.

Essa identificação ocorre por meio de uma palavra e emoji que identifica se aquele commit realizado se trata de uma alteração de código, atualização de pacotes, documentação, alteração de visual, teste...

---
## Tipo e descrição 🦄

O commit semântico possui os elementos estruturais abaixo (tipos), que informam a intenção do seu commit ao utilizador(a) de seu código.

- `feat`- Commits do tipo feat indicam que seu trecho de código está incluindo um **novo recurso** (se relaciona com o MINOR do versionamento semântico).

- `fix` - Commits do tipo fix indicam que seu trecho de código commitado está **solucionando um problema** (bug fix), (se relaciona com o PATCH do versionamento semântico).

- `docs` - Commits do tipo docs indicam que houveram **mudanças na documentação**, como por exemplo no Readme do seu repositório. (Não inclui alterações em código).

- `test` - Commits do tipo test são utilizados quando são realizadas **alterações em testes**, seja criando, alterando ou excluindo testes unitários. (Não inclui alterações em código)

- `build` - Commits do tipo build são utilizados quando são realizadas modificações em **arquivos de build e dependências**.

- `perf` - Commits do tipo perf servem para identificar quaisquer alterações de código que estejam relacionadas a **performance**.

- `style` - Commits do tipo style indicam que houveram alterações referentes a **formatações de código**, semicolons, trailing spaces, lint... (Não inclui alterações em código).

- `refactor` - Commits do tipo refactor referem-se a mudanças devido a **refatorações que não alterem sua funcionalidade**, como por exemplo, uma alteração no formato como é processada determinada parte da tela, mas que manteve a mesma funcionalidade, ou melhorias de performance devido a um code review.

- `chore` - Commits do tipo chore indicam **atualizações de tarefas** de build, configurações de administrador, pacotes... como por exemplo adicionar um pacote no gitignore. (Não inclui alterações em código)

- `ci` - Commits do tipo ci indicam mudanças relacionadas a **integração contínua** (_continuous integration_).

- `raw` - Commits to tipo raw indicam mudanças relacionadas a arquivos de configurações, dados, features, parametros.

---
  
## Recomendações 🎉

- Adicione um tipo consistente com o título do conteúdo.
- Recomendamos que na primeira linha deve ter no máximo 4 palavras.
- Para descrever com detalhes, usar a descrição do commit.
- Usar um emoji no início da mensagem de commit representando sobre o commit.
- Os links precisam ser adicionados em sua forma mais autêntica, ou seja: sem encurtadores de link e links afiliados.

---

## Complementos de commits 💻

- **Rodapé:** informação sobre o revisor e número do card no Trello ou Jira. Exemplo: Reviewed-by: Elisandro Mello Refs #133
- **Corpo:** descrições mais precisas do que está contido no commit, apresentando impactos e os motivos pelos quais foram empregadas as alterações no código, como também instruções essenciais para intervenções futuras. Exemplo: see the issue for details on typos fixed.
- **Descrições:** uma descrição sucinta da mudança. Exemplo: correct minor typos in code

---

## Padrões de emojis 💈

<table>
  <thead>
    <tr>
      <th>Tipo do commit</th>
      <th>Emoji</th>
      <th>Palavra-chave</th>
    </tr>
  </thead>
 <tbody>
    <tr>
      <td>Acessibilidade</td>
      <td>♿ <code>:wheelchair:</code></td>
      <td></td>
    </tr>
    <tr>
      <td>Adicionando um teste</td>
      <td>✅ <code>:white_check_mark:</code></td>
      <td><code>test</code></td>
    </tr>
    <tr>
      <td>Adicionando uma dependência</td>
      <td>➕ <code>:heavy_plus_sign:</code></td>
      <td><code>build</code></td>
    </tr>
    <tr>
      <td>Alterações de revisão de código</td>
      <td>👌 <code>:ok_hand:</code></td>
      <td><code>style</code></td>
    </tr>
    <tr>
      <td>Animações e transições</td>
      <td>💫 <code>:dizzy:</code></td>
      <td></td>
    </tr>
    <tr>
      <td>Bugfix</td>
      <td>🐛 <code>:bug:</code></td>
      <td><code>fix</code></td>
    </tr>
    <tr>
      <td>Comentários</td>
      <td>💡 <code>:bulb:</code></td>
      <td><code>docs</code></td>
    </tr>
    <tr>
      <td>Commit inicial</td>
      <td>🎉 <code>:tada:</code></td>
      <td><code>init</code></td>
    </tr>
    <tr>
      <td>Configuração</td>
      <td>🔧 <code>:wrench:</code></td>
      <td><code>chore</code></td>
    </tr>
    <tr>
      <td>Deploy</td>
      <td>🚀 <code>:rocket:</code></td>
      <td></td>
    </tr>
    <tr>
      <td>Documentação</td>
      <td>📚 <code>:books:</code></td>
      <td><code>docs</code></td>
    </tr>
    <tr>
      <td>Em progresso</td>
      <td>🚧 <code>:construction:</code></td>
      <td></td>
    </tr>
    <tr>
      <td>Estilização de interface</td>
      <td>💄 <code>:lipstick:</code></td>
      <td><code>feat</code></td>
    </tr>
    <tr>
      <td>Infraestrutura</td>
      <td>🧱 <code>:bricks:</code></td>
      <td><code>ci</code></td>
    </tr>
    <tr>
      <td>Lista de ideias (tasks)</td>
      <td>🔜 <code> :soon: </code></td>
      <td></td>
    </tr>
    <tr>
      <td>Mover/Renomear</td>
      <td>🚚 <code>:truck:</code></td>
      <td><code>chore</code></td>
    </tr>
    <tr>
      <td>Novo recurso</td>
      <td>✨ <code>:sparkles:</code></td>
      <td><code>feat</code></td>
    </tr>
    <tr>
      <td>Package.json em JS</td>
      <td>📦 <code>:package:</code></td>
      <td><code>build</code></td>
    </tr>
    <tr>
      <td>Performance</td>
      <td>⚡ <code>:zap:</code></td>
      <td><code>perf</code></td>
    </tr>
    <tr>
        <td>Refatoração</td>
        <td>♻️ <code>:recycle:</code></td>
        <td><code>refactor</code></td>
    </tr>
    <tr>
      <td>Removendo um arquivo</td>
      <td>🔥 <code>:fire:</code></td>
      <td></td>
    </tr>
    <tr>
      <td>Removendo uma dependência</td>
      <td>➖ <code>:heavy_minus_sign:</code></td>
      <td><code>build</code></td>
    </tr>
    <tr>
      <td>Responsividade</td>
      <td>📱 <code>:iphone:</code></td>
      <td></td>
    </tr>
    <tr>
      <td>Revertendo mudanças</td>
      <td>💥 <code>:boom:</code></td>
      <td><code>fix</code></td>
    </tr>
    <tr>
      <td>Segurança</td>
      <td>🔒️ <code>:lock:</code></td>
      <td></td>
    </tr>
    <tr>
      <td>SEO</td>
      <td>🔍️ <code>:mag:</code></td>
      <td></td>
    </tr>
    <tr>
      <td>Tag de versão</td>
      <td>🔖 <code>:bookmark:</code></td>
      <td></td>
    </tr>
    <tr>
      <td>Teste de aprovação</td>
      <td>✔️ <code>:heavy_check_mark:</code></td>
      <td><code>test</code></td>
    </tr>
    <tr>
      <td>Testes</td>
      <td>🧪 <code>:test_tube:</code></td>
      <td><code>test</code></td>
    </tr>
    <tr>
      <td>Texto</td>
      <td>📝 <code>:pencil:</code></td>
      <td></td>
    </tr>
    <tr>
      <td>Tipagem</td>
      <td>🏷️ <code>:label:</code></td>
      <td></td>
    </tr>
    <tr>
      <td>Tratamento de erros</td>
      <td>🥅 <code>:goal_net:</code></td>
      <td></td>
    </tr>
   <tr>
      <td>Dados</td>
      <td>🗃️ <code>:card_file_box:</code></td>
      <td><code>raw</code></td>
    </tr>
  </tbody>
</table>

---

## 💻 Exemplos

<table>
  <thead>
    <tr>
      <th>Comando Git</th>
      <th>Resultado no GitHub</th>
    </tr>
  </thead>
 <tbody>
    <tr>
      <td>
        <code>git commit -m ":tada: Commit inicial"</code>
      </td>
      <td>🎉 Commit inicial</td>
    </tr>
    <tr>
      <td>
        <code>git commit -m ":books: docs: Atualização do README"</code>
      </td>
      <td>📚 docs: Atualização do README</td>
    </tr>
    <tr>
      <td>
        <code>git commit -m ":bug: fix: Loop infinito na linha 50"</code>
      </td>
      <td>🐛 fix: Loop infinito na linha 50</td>
    </tr>
    <tr>
      <td>
        <code>git commit -m ":sparkles: feat: Página de login"</code>
      </td>
      <td>✨ feat: Página de login</td>
    </tr>
    <tr>
      <td>
        <code>git commit -m ":bricks: ci: Modificação no Dockerfile"</code>
      </td>
      <td>🧱 ci: Modificação no Dockerfile</td>
    </tr>
    <tr>
      <td>
        <code>git commit -m ":recycle: refactor: Passando para arrow functions"</code>
      </td>
      <td>♻️ refactor: Passando para arrow functions</td>
    </tr>
    <tr>
      <td>
        <code>git commit -m ":zap: perf: Melhoria no tempo de resposta"</code>
      </td>
      <td>⚡ perf: Melhoria no tempo de resposta</td>
    </tr>
    <tr>
      <td>
        <code>git commit -m ":boom: fix: Revertendo mudanças ineficientes"</code>
      </td>
      <td>💥 fix: Revertendo mudanças ineficientes</td>
    </tr>
    <tr>
      <td>
        <code>git commit -m ":lipstick: feat: Estilização CSS do formulário"</code>
      </td>
      <td>💄 feat: Estilização CSS do formulário</td>
    </tr>
    <tr>
      <td>
        <code>git commit -m ":test_tube: test: Criando novo teste"</code>
      </td>
      <td>🧪 test: Criando novo teste</td>
    </tr>
    <tr>
      <td>
        <code>git commit -m ":bulb: docs: Comentários sobre a função LoremIpsum( )"</code>
      </td>
      <td>💡 docs: Comentários sobre a função LoremIpsum( )</td>
    </tr>
    <tr>
      <td>
        <code>git commit -m ":bulb: raw: RAW Data do ano aaaa"</code>
      </td>
      <td>🗃️ raw: RAW Data do ano aaaa</td>
    </tr>
  </tbody>
</table>

---
