# ☕ Java Red Hat Base — ambiente leve e otimizado para desenvolvimento Java no VS Code

**Um ambiente de desenvolvimento Java e Spring Boot (Maven) completo, estável e otimizado para máquinas modestas com Sistema Operacional Windows.** Criado com base na **Stack Red Hat**, este projeto busca oferecer uma alternativa **leve, limpa e eficiente** para quem deseja programar em Java usando o **Visual Studio Code**.

## 🧭 Sobre o projeto

Este repositório nasceu de um desafio pessoal: **criar um ambiente Java profissional e fluido em um notebook simples**, sem abrir mão das boas práticas de código, da estrutura moderna de desenvolvimento e do conforto visual.

Durante minha jornada de estudos em **backend com Java**, percebi que muitas configurações disponíveis na internet partem do pressuposto de que o desenvolvedor tem uma máquina robusta — o que não é a realidade de todos.  

Assim, comecei a construir o meu próprio ambiente: enxuto, rápido e organizado.  

O resultado é este projeto, que agora compartilho para ajudar outros desenvolvedores e estudantes que estão na mesma caminhada.

## 🎯 Objetivo

O propósito do **Java Red Hat Base** é entregar um ambiente pronto para trabalhar com **Java puro** e **Spring Boot**, sem precisar de configurações complexas.

Este setup foi pensado para quem quer:

✔️ Um **ambiente leve**, que roda bem até em notebooks básicos;  
✔️ Um **setup didático**, que explica cada ajuste e sua função;  
✔️ Uma **base confiável para estudos e projetos reais**;  
✔️ Um **padrão visual e de código consistente**, inspirado no ecossistema da `JetBrains` (IntelliJ IDEA).

## 💻 Contexto do ambiente base

Todo o ambiente foi projetado e testado em uma máquina simples — o que reforça a proposta de **eficiência e acessibilidade**:

| Componente | Especificação |
|-------------|---------------|
| **Modelo** | Positivo Stilo XC3650 |
| **Processador** | Intel Celeron N3010 |
| **Memória RAM** | 4 GB |
| **Armazenamento** | SSD 120 GB |
| **Sistema Operacional** | Windows 10 Pro 64 bits |
| **IDE** | Visual Studio Code |
| **JDK** | Versão 25 (Oracle) |

Mesmo com essa configuração modesta, o ambiente roda **com estabilidade, agilidade e total compatibilidade com o ecossistema Java moderno**.

## 📘 Estrutura do guia

O projeto foi dividido em **5 passos práticos e diretos**, para que você possa montar seu ambiente do zero com segurança:

✔️ **Configurando o ambiente Java**;  
✔️ **Baixando e instalando a fonte JetBrains Mono**;  
✔️ **Preparando o ambiente de desenvolvimento no VS Code**;  
✔️ **Configurando o User Settings (arquivo JSON)**;  
✔️ **Aplicando otimizações e dicas adicionais**.

---

## ☕ 1° Passo — Instalando o JDK no Windows

Antes de começar a configurar o Visual Studio Code, é fundamental garantir que o **Java Development Kit (JDK)** esteja instalado corretamente no seu computador.

O **JDK** é o conjunto de ferramentas que permite **compilar, executar e depurar programas Java**. Sem ele, o VS Code não conseguirá reconhecer nem executar seu código Java.

### 🧩 Verificação prévia

Se você **já possui o JDK instalado** e **as variáveis de ambiente `JAVA_HOME` e `Path` configuradas corretamente**, pode **pular este passo** e seguir direto para a configuração do ambiente no VS Code.

💡 Para verificar, abra o **Terminal** (PowerShell ou Prompt de Comando) e digite:

```
java -version
echo %JAVA_HOME%
``` 
> Se ambos os comandos retornarem resultados válidos, o JDK está instalado e configurado corretamente.

### 📥 Download do JDK

Se o seu computador **ainda não possui o JDK instalado**, acesse o site oficial da `Oracle` e baixe a versão mais recente do Java SE Development Kit (recomenda-se a versão 25 LTS).

👉 [Baixar o JDK — Oracle Java](https://www.oracle.com/br/java/technologies/downloads/)

### 🎓 Instalação passo a passo no Windows

Após o download, siga o tutorial abaixo, que explica **como instalar o JDK e configurar as variáveis `JAVA_HOME` e `Path`** de forma simples e visual:

👉 [Tutorial completo — Como instalar o JDK no Windows (YouTube)](https://www.youtube.com/watch?v=cT_VDy5TKTA)

> O vídeo mostra exatamente o processo que usei neste projeto, incluindo a criação da variável de ambiente `JAVA_HOME` e a adição do caminho `bin` no `Path`, que são indispensáveis para que o VS Code reconheça o JDK corretamente.

---

## 🖋️ 2° Passo — Instalando a Fonte JetBrains Mono

Um bom ambiente de desenvolvimento vai além do código: a legibilidade faz toda a diferença na produtividade e no conforto visual.

Por isso, este projeto utiliza a **JetBrains Mono**, uma fonte criada especialmente para programadores.

Ela facilita a leitura, diferencia melhor caracteres semelhantes (como `O` e `0`, `l` e `1`) e oferece espaçamento ideal para código.

### 📥 Download da Fonte

Acesse o site oficial da JetBrains para baixar a fonte:

👉 [Baixar JetBrains Mono — Site Oficial](https://www.jetbrains.com/lp/mono/)

Na página, clique em **Download** e aguarde o download do arquivo ZIP.

### 📁 Organização da Pasta

Para manter a organização, crie manualmente uma pasta específica para armazenar a fonte no seu computador.  

Caminho recomendado:

```
C:\Program Files\JetBrains Mono
```

1. Extraia o conteúdo do arquivo ZIP que você baixou para dentro dessa pasta (`C:\Program Files\JetBrains Mono`);
2. Acesse a subpasta `fonts`, depois abra `ttf`;  
3. Selecione todos os arquivos (`Ctrl + A`), clique com o botão direito do mouse e escolha **Instalar para todos os usuários**.  

Aguarde a instalação concluir.

---

## 🧰 3° Passo — Preparando o Ambiente de Desenvolvimento no VS Code

Com o **JDK** e a **fonte JetBrains Mono** instalados, chegou o momento de configurar o **Visual Studio Code** para o desenvolvimento em **Java**.  
Este passo transforma o VS Code em uma IDE Java completa, leve e eficiente, totalmente otimizada para rodar bem em máquinas simples.

### ⚙️ Criando o Profile "Java Red Hat Base"

1. No canto inferior esquerdo, clique em **⚙️ → Profiles → Create Profile**.  
2. Na janela que abrir, preencha assim:

| Campo | O que escolher | Motivo |
|--------|----------------|--------|
| **Name** | `Java Red Hat Base` | Identificação do ambiente Java |
| **Icon** | Escolha o ícone de sua preferência | É opcional |
| **Copy from** | `None` | Cria um perfil limpo, sem heranças |
| **Settings** | `None` | Vamos colar o JSON do projeto |
| **Keyboard Shortcuts** | `None` | Evita conflitos de atalhos |
| **Tasks** | `None` | O VS Code gera automaticamente para Java |
| **MCP Servers** | `None` | Não necessário |
| **Snippets** | `None` | Pode adicionar depois, se quiser |
| **Extensions** | `None` | Instalaremos manualmente as essenciais |

3. Clique em **Create**.  
4. Verifique se aparece o status **✔ Active** ao lado do nome.

> 💡 **Dica:** Escolher “None” em tudo garante um perfil completamente limpo, perfeito para aplicar apenas as configurações otimizadas do projeto.

### 🧩 Instalando as extensões essenciais

Com o perfil criado, o próximo passo é instalar as extensões que transformarão o VS Code em uma IDE completa para **Java** e **Spring Boot**.

#### 🔹 1. Extension Pack for Java  
👉 [Baixar no Marketplace](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-debug)

Este pacote oficial da **Microsoft e Red Hat** instala todas as ferramentas essenciais:

- **Language Support for Java™ (by Red Hat)** — suporte completo à linguagem Java;  
- **Debugger for Java** — depurador integrado;  
- **Test Runner for Java** — executa testes JUnit;  
- **Maven for Java** — integração com projetos Maven;  
- **Project Manager for Java** — gerencia dependências e estrutura do projeto;  
- **Visual Studio IntelliCode** — sugestões inteligentes.

#### 🔹 2. Spring Boot Extension Pack  
👉 [Baixar no Marketplace](https://marketplace.visualstudio.com/items?itemName=vmware.vscode-boot-dev-pack)

Voltado para quem vai trabalhar com **Spring Boot**, o framework Java mais popular para back-end.  

Esse pacote instala automaticamente:

- **Spring Boot Dashboard** — gerencia e executa aplicações Spring direto do VS Code;  
- **Spring Boot Tools** — auxilia no desenvolvimento e debug;  
- **Spring Initializr Java Support** — cria novos projetos Spring Boot facilmente.

> 💡 Mesmo que você ainda não use o Spring, é interessante deixar o ambiente preparado.

#### 🔹 3. SonarQube for IDE (SonarLint)  
👉 [Baixar no Marketplace](https://marketplace.visualstudio.com/items?itemName=SonarSource.sonarlint-vscode)

O **SonarLint** analisa o código em tempo real e aponta problemas, más práticas e vulnerabilidades.  
É uma excelente ferramenta para quem quer escrever código limpo e profissional.

Principais funções:

- Análise estática local (sem precisar de servidor);  
- Sugestões de melhoria e correções automáticas (Quick Fix);  
- Pode ser conectado ao SonarQube Cloud para projetos em equipe.

> 💡 **Dica:** É como ter um mentor silencioso analisando seu código e te ensinando boas práticas.

#### 🔹 4. JetBrains Theme (opcional)  
👉 [Baixar no Marketplace](https://marketplace.visualstudio.com/items?itemName=kenethriera.jb-theme)

Tema escuro inspirado no IntelliJ IDEA, com contraste equilibrado e ótimo para longas sessões de trabalho.

#### 🔹 5. JetBrains Icon Theme (opcional)  
👉 [Baixar no Marketplace](https://marketplace.visualstudio.com/items?itemName=chadalen.vscode-jetbrains-icon-theme)

Adiciona ícones de pastas e arquivos no estilo JetBrains, deixando o ambiente mais agradável e organizado.

> 💡 Pronto! Seu VS Code estará visualmente idêntico ao IntelliJ IDEA, mas muito mais leve e rápido. Com o ambiente configurado, o próximo passo será aplicar o **User Settings (JSON)** do projeto — onde ajustaremos o desempenho, a estética e o comportamento interno do VS Code.

---

## ⚙️ 4° Passo — Aplicando o User Settings (JSON)

Este passo é responsável por ajustar **toda a interface, comportamento e desempenho interno do VS Code** para desenvolvimento em **Java e Spring Boot**, garantindo fluidez mesmo em máquinas modestas.

---

### ⚠️ Como aplicar o arquivo de configuração

1. **Copie** todo o conteúdo do arquivo `user-settings.json` (disponível neste repositório);  
2. No **VS Code**, certifique-se de que o **Profile Java Red Hat Base** está ativo:
```
- Clique no ícone de engrenagem (⚙️) → **Profiles** → selecione **Java Red Hat Base**;  
```
3. Pressione **F1** (ou `Ctrl + Shift + P`) e digite: `Open User Settings (JSON)` → Pressione **Enter**;  
4. **Cole** o conteúdo copiado **substituindo todo o texto existente**;  
5. Pressione **`Ctrl + S`** para **salvar**;  
6. Se o VS Code solicitar **reinicialização**, **confirme**. Isso garante que todas as configurações sejam aplicadas corretamente.

### 🧩 Estrutura e explicação do arquivo

#### 1. Workbench & Explorer (Interface do VS Code)
Configura aparência e comportamento da interface:
- `"workbench.startupEditor": "newUntitledFile"` → abre o VS Code com um arquivo novo e vazio.  
- `"workbench.editor.labelFormat": "short"` → exibe nomes curtos nas abas.  
- `"workbench.editor.showTabs": "multiple"` → permite várias abas simultâneas.  
- `"workbench.iconTheme": "vscode-jetbrains-icon-theme-2023-dark"` → aplica ícones no estilo JetBrains.  
- `"workbench.colorTheme": "JetBrains Dark Theme"` → usa tema escuro agradável aos olhos.  
- `"explorer.compactFolders": false"` → exibe cada pasta separadamente (melhor visualização em `src/main/java`).  
- `"explorer.confirmDragAndDrop": false"` → evita pop-ups ao mover pastas no explorador.

#### 2. Editor (Legibilidade e produtividade)
Ajustes de fonte, formatação e comportamento:
- `"editor.fontFamily": "JetBrains Mono"` → fonte otimizada para código.  
- `"editor.fontLigatures": true"` → exibe ligações tipográficas (como `==`, `!=`, `=>`).  
- `"editor.fontSize": 13"` → tamanho equilibrado e legível.  
- `"editor.lineHeight": 1.2"` → altura de linha compacta.  
- `"editor.rulers": [100]"` → régua de 100 colunas, seguindo o **Google Java Style**.  
- `"editor.renderLineHighlight": "gutter"` → realce discreto da linha atual.  
- `"editor.minimap.enabled": false"` → desativa o minimapa, economizando memória.  
- `"editor.semanticHighlighting.enabled": true"` → cores diferentes para variáveis, classes e métodos.  
- `"editor.parameterHints.enabled": true"` → mostra assinaturas de métodos enquanto digita.  
- `"editor.formatOnSave": true"` → formata automaticamente ao salvar.  
- `"editor.suggestSelection": "recentlyUsedByPrefix"` → prioriza sugestões que você usa com frequência.  
- `"editor.quickSuggestions"` → ativa sugestões no código, mas desativa em comentários e strings.

#### 3. Java (Ambiente e performance)
Configura o runtime, memória e padrão de formatação:
- `"java.jdt.ls.java.home": "${env:JAVA_HOME}"` → usa o JDK definido no sistema.  
- `"java.configuration.runtimes"` → define o Java 25 como padrão.  
- `"java.jdt.ls.vmargs"` → otimiza o **Language Server** com flags para máquinas simples:
- `-XX:+UseParallelGC` → coletor de lixo rápido.  
- `-XX:GCTimeRatio=4` → foco em responsividade.  
- `-Xms128m` / `-Xmx512m` → uso reduzido de memória.  
- `-Dsun.zip.disableMemoryMapping=true` → evita travamentos em I/O.  
- `"java.format.settings.url"` → aplica o **Google Java Style**.  
- `"java.format.settings.profile": "GoogleStyle"` → seleciona o perfil correto.  
- `"[java]": { "editor.defaultFormatter": "redhat.java" }` → usa o formatador da Red Hat.

#### 4. Build & Import (Maven)
- `"java.import.maven.enabled": true"` → ativa import automático de projetos Maven.  
- `"java.import.gradle.enabled": false"` → desativa Gradle para economizar recursos.  
- `"java.maxConcurrentBuilds": 1"` → evita sobrecarga de CPU em builds simultâneos.  
- `"java.configuration.updateBuildConfiguration": "automatic"` → reimporta dependências automaticamente.  
- `"java.errors.incompleteClasspath.severity": "ignore"` → reduz alertas durante o carregamento inicial.

#### 5. Extensões & Telemetria
- `"extensions.ignoreRecommendations": true"` → evita pop-ups de recomendações.  
- `"redhat.telemetry.enabled": false` e similares → desativa coleta de dados e uso de CPU desnecessário.

#### 6. Files & Search
- `"files.exclude"` → oculta arquivos e pastas desnecessários (`target`, `.classpath`, etc.).  
- `"search.smartCase": true"` → busca inteligente com distinção de maiúsculas apenas quando usado.

#### 7. Terminal Integrado
- `"terminal.integrated.gpuAcceleration": "auto"` → aceleração automática via GPU.  
- `"terminal.integrated.fontFamily": "JetBrains Mono"` → mantém consistência visual.  
- `"terminal.integrated.cursorBlinking": true"` → cursor com destaque visível.

#### 8. Git (Boas práticas)
- `"git.enableSmartCommit": false"` → evita commits automáticos.  
- `"git.autofetch": true"` / `"git.pruneOnFetch": true"` → mantém histórico remoto atualizado.  
- `"git.allowForcePush": false"` → previne perda de histórico.  
- `"git.confirmSync": true"` → pede confirmação antes de sincronizar.  

### ✅ Conclusão do 4º passo

Após aplicar o `user-settings.json`, o VS Code estará totalmente configurado para um ambiente **Java Red Hat Base**: rápido, visualmente limpo e funcional mesmo em notebooks básicos. Essas configurações padronizam a experiência de desenvolvimento, aumentam a produtividade e reduzem travamentos, oferecendo **uma IDE Java completa dentro do VS Code** — com o equilíbrio ideal entre desempenho, estética e boas práticas.

---

## 🚀 5º Passo — Dicas extrar de otimizações para desempenho

Este passo traz **ajustes opcionais**, com foco em **máquinas com 4 GB de RAM** e no **fluxo de iniciantes**. Cada dica vem com **passo a passo** e **impacto prático**.

### 5.1 — Tornar o formatter offline (Google Style XML local)

**Objetivo:** impedir que o VS Code **baixe o XML do Google Java Style** a cada inicialização — isso **reduz I/O e latência**, deixando o ambiente mais previsível e rápido.

#### Onde baixar o XML oficial

- [Repositório oficial do Google Styleguide:](https://github.com/google/styleguide)

- [XML do perfil (link direto)](https://github.com/google/styleguide/blob/gh-pages/eclipse-java-google-style.xml)

#### Passo a passo

1. **Crie** a pasta local para guardar o XML:

```
C:\SystemTools\Java\
```
2. **Baixe** o XML do link acima e **salve** como:

```
C:\SystemTools\Java\google-style.xml
````
3. Abra o VS Code e **ative** o profile **Java Red Hat Base**;
4. Pressione **F1** (ou `Ctrl+Shift+P`) → `Open User Settings (JSON)` → **Enter**;
5. Localize o trecho do formatter no `JSON` e **substitua** o bloco existente pelo abaixo:

**ANTES (arquivo remoto):**

```
"java.format.settings.url": "https://raw.githubusercontent.com/google/styleguide/gh-pages/eclipse-java-google-style.xml",
"java.format.settings.profile": "GoogleStyle"
```

**DEPOIS (arquivo local — recomendado):**

```
"java.format.settings.url": "file:///C:/SystemTools/Java/google-style.xml",
"java.format.settings.profile": "GoogleStyle"
```

6. **Salve** e **reinicie** o VS Code se solicitado.

> **Impacto:** o formatador será carregado diretamente do disco, evitando depender da internet e tornando o carregamento do ambiente mais rápido e estável.

### 5.4 — Dicas adicionais de otimização (interface e desempenho visual)

Essas dicas reduzem o consumo de memória, CPU e distrações visuais. Você pode aplicá-las pela **interface gráfica (Settings UI)** ou diretamente no `User Settings (JSON)`. Todas podem ser revertidas facilmente se desejar restaurar o visual padrão.

#### 🧭 A) Desativar telemetria do VS Code

**Via interface:**

1. Vá em `File` → `Preferences` → `Settings`;
2. Busque por `telemetry`;
3. Desative todas as opções ou defina `Telemetry Level` como **off**.

> **Impacto:** reduz tráfego de rede e uso de threads em segundo plano.

#### 🧭 B) Desativar rolagem suave (smooth scrolling)

**Via interface:**

1. Vá em `File` → `Preferences` → `Settings`;
2. Busque por `smoothScrolling`;
3. Desmarque a opção `Window: Smooth Scrolling`.

**Via JSON:**

```
"window.smoothScrolling": false
```

> **Impacto:** rolagem mais direta e responsiva, ideal em notebooks modestos.

#### 🧭 C) Reduzir elementos visuais (para foco e leveza)

Essas configurações escondem elementos da interface que consomem espaço e processamento.

**Ocultar a barra lateral de ícones (Activity Bar):**

**Via interface:** `View` → `Appearance` → `Activity Bar` (alternar)

**Via JSON:**

```
"workbench.activityBar.visible": false
```

**Desativar Breadcrumbs (trilha de navegação no topo):**

**Via interface:** `View` → `Appearance` → `Breadcrumbs` (alternar)

**Via JSON:**

```
"breadcrumbs.enabled": false
```

> **Impacto:** ambiente visual mais limpo e fluido, especialmente em telas pequenas.

#### 🧭 D) Controlar extensões e atualizações automáticas

**Via interface:** `Ctrl+Shift+X` → `Manage (⚙)` → `Disable/Uninstall` as extensões que você não usa.

**Via JSON (para controle de updates):**

```
"extensions.autoUpdate": false
```

> **Impacto:** evita processos em segundo plano e reindexações desnecessárias.

#### 🧭 E) Solucionar lentidão do Java Language Server

Se o VS Code estiver travando ou não sugerindo código:

1. Pressione **F1**;
2. Digite **Java: Clean Java Language Server Workspace**;
3. Pressione **Enter** e confirme o **Reload Window**.

> **Impacto:** limpa o cache e resolve problemas de indexação sem reinstalar nada.

---

## ✅ Encerramento

Parabéns! 🎉

Você concluiu toda a configuração do ambiente **Java Red Hat Base** — um setup leve, visualmente limpo e funcional, ideal para máquinas simples e para quem está começando no desenvolvimento Java.

Se este projeto te ajudou, considere **deixar uma estrela (⭐)** no repositório.

Fique à vontade para **abrir issues**, **enviar PRs** ou **deixar sugestões de melhoria**.

💬 Dúvidas, ideias ou otimizações?

Compartilhe nos comentários do repositório — será um prazer trocar experiências e aprimorar juntos o ambiente!