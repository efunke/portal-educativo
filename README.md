# Portal Educativo - v1.0
Data: 20/10/2026
Autor: Edson Funke

Portal de códigos, exemplos e materiais de apoio para atividades educacionais e projetos de programação.

## 1. Estrutura do projeto

```text
portal-educativo/
├── .gitignore
├── LICENSE
├── README.md
├── assuntos/
│   ├── sorteio-assuntos-2026-10-20.txt
│   ├── grupo-01/
│   ├── grupo-02/
│   ├── grupo-03/
│   ├── grupo-04/
│   ├── grupo-05/
│   ├── grupo-06/
│   ├── grupo-07/
│   ├── grupo-08/
│   ├── grupo-09/
│   └── grupo-10/
├── comandos/
│   └── basico-01.png
└── etapas/
    ├── como-usar-estilo.md
    ├── estrutura-conteudo-assuntos.md
    ├── menu.md
    ├── modelo-controle.md
    ├── modelo-style-portal-educacional.css
    ├── modelo-system-design-educacional.md
    └── regras.md
```

### 1.1 Descrição dos diretórios

| Diretório / arquivo | Descrição |
|---|---|
| `assuntos/` | Organização dos assuntos e materiais distribuídos entre os grupos. |
| `assuntos/grupo-01/` a `grupo-10/` | Diretórios destinados aos materiais de cada grupo. |
| `comandos/` | Imagens e materiais de referência sobre comandos. |
| `etapas/` | Documentação, orientações e modelos utilizados nas atividades. |
| `README.md` | Documento principal de apresentação e orientação do projeto. |
| `.gitignore` | Define arquivos e diretórios que não devem ser rastreados pelo Git. |
| `LICENSE` | Informa as condições de uso, distribuição e modificação do projeto. |

## 2. Pré-requisitos

Para utilizar o projeto, é necessário ter o Git instalado no computador.

Verifique a instalação abrindo o PowerShell ou o CMD e executando:

```powershell
git --version
```

Se o comando retornar a versão instalada, o Git está disponível no terminal.

## 3. Comandos básicos do Git

### 3.1 Clonar o repositório

A clonagem cria uma cópia local do repositório remoto no computador.

**Passo 1 — Abrir o terminal**

Abra o PowerShell ou o CMD e acesse o diretório em que deseja armazenar os projetos:

```powershell
cd C:\dev\src
```

Ajuste o caminho conforme a organização de diretórios do seu computador.

**Passo 2 — Clonar o repositório**

```powershell
git clone https://github.com/efunke/portal-educativo.git
```

**Passo 3 — Entrar no diretório do projeto**

```powershell
cd portal-educativo
```

**Passo 4 — Verificar a situação do repositório**

```powershell
git status
```

Esse comando informa se existem alterações locais pendentes e em qual branch você está trabalhando.

### 3.2 Atualizar o repositório local

Antes de começar a trabalhar, atualize sua cópia local com as alterações disponíveis no GitHub:

```powershell
git pull
```

Execute o comando dentro do diretório do projeto.

Se houver alterações locais conflitantes com as alterações remotas, o Git poderá solicitar a resolução de conflitos antes de concluir a atualização.

### 3.3 Verificar as alterações

Depois de criar ou modificar arquivos, consulte o estado do repositório:

```powershell
git status
```

Para visualizar as diferenças nos arquivos já rastreados pelo Git:

```powershell
git diff
```

Revise as alterações antes de registrá-las.

### 3.4 Preparar arquivos para o commit

O comando `git add` seleciona as alterações que farão parte do próximo commit.

Para adicionar um arquivo específico:

```powershell
git add README.md
```

Para adicionar um arquivo de uma pasta:

```powershell
git add etapas/menu.md
```

Para adicionar todas as alterações do diretório atual:

```powershell
git add .
```

**Recomendação:** prefira adicionar arquivos específicos quando possível, principalmente em atividades educacionais. Isso ajuda a evitar o envio acidental de arquivos temporários ou de alterações que não fazem parte da atividade.

### 3.5 Registrar as alterações

O comando `git commit` registra um conjunto de alterações no histórico local do repositório.

```powershell
git commit -m "docs: atualiza documentação do projeto"
```

Escreva mensagens curtas e claras, descrevendo o que foi alterado.

Exemplos:

```powershell
git commit -m "docs: adiciona orientações de Git"
git commit -m "style: atualiza modelo CSS"
git commit -m "docs: corrige estrutura do projeto"
```

O commit é realizado localmente; ele ainda não envia as alterações ao GitHub.

### 3.6 Enviar as alterações ao GitHub

Para enviar os commits locais ao repositório remoto:

```powershell
git push
```

O envio depende das permissões de acesso ao repositório e da configuração da branch atual.

Se o aluno não tiver permissão de escrita no repositório original, poderá ser necessário trabalhar em um fork e enviar as alterações por meio de um Pull Request.

### 3.7 Consultar o histórico

Para visualizar os commits recentes:

```powershell
git log --oneline
```

Esse comando apresenta uma lista resumida das alterações registradas no histórico.

## 4. Fluxo de trabalho recomendado

Para uma atividade comum de manutenção da documentação, siga esta sequência:

```powershell
# 1. Entrar no projeto
cd C:\dev\src\portal-educativo

# 2. Atualizar a cópia local
git pull

# 3. Verificar o estado do repositório
git status

# 4. Editar os arquivos necessários
# Utilize seu editor de código preferido.

# 5. Revisar as alterações
git diff

# 6. Preparar o arquivo alterado
git add README.md

# 7. Registrar as alterações
git commit -m "docs: atualiza README"

# 8. Enviar ao GitHub
git push
```

Substitua `README.md` pelo arquivo efetivamente modificado.

**Importante:** não execute `git add .` ou `git push` automaticamente sem revisar as alterações e verificar se você tem autorização para enviá-las.

## 5. Boas práticas

- Atualize sua cópia local antes de iniciar uma atividade.
- Faça alterações pequenas e relacionadas a um objetivo específico.
- Utilize mensagens de commit claras e descritivas.
- Revise os arquivos antes de adicioná-los ao commit.
- Não versione senhas, tokens, chaves privadas ou outros segredos.
- Não inclua arquivos temporários, dependências instaladas ou arquivos pessoais sem necessidade.
- Respeite a organização de diretórios e os padrões definidos para o projeto.
- Em caso de dúvidas ou conflitos, consulte o professor antes de executar comandos que possam descartar alterações.

## 6. Documentação complementar

Consulte os arquivos da pasta `etapas/` para obter orientações e modelos específicos das atividades:

- `regras.md` — regras e orientações do projeto.
- `menu.md` — documentação do menu.
- `estrutura-conteudo-assuntos.md` — organização dos conteúdos e assuntos.
- `como-usar-estilo.md` — orientações para utilizar estilos CSS.
- `modelo-controle.md` — modelo de documentação de controle.
- `modelo-style-portal-educacional.css` — modelo básico de CSS.
- `modelo-system-design-educacional.md` — modelo de documentação de arquitetura de sistemas.

## 7. Referência oficial

Repositório no GitHub:

https://github.com/efunke/portal-educativo.git

Para consultar a documentação oficial do Git:

https://git-scm.com/doc

---

*Documento destinado a orientar estudantes no uso do repositório e na aprendizagem dos conceitos básicos de versionamento com Git.*
