# ☕ Java Red Hat Base — ambiente leve e otimizado para desenvolvimento Java no VS Code

**Um ambiente de desenvolvimento Java e Spring Boot completo, estável e otimizado para máquinas modestas com Sistema Operacional Windows.** Criado com base na **Stack Red Hat**, este projeto busca oferecer uma alternativa **leve, limpa e eficiente** para quem deseja programar em Java usando o **Visual Studio Code**.

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
✔️ Um **padrão visual e de código consistente**, inspirado no ecossistema da JetBrains (IntelliJ IDEA).

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
| **JDK** | Versão 25 (Oracle / Red Hat) |

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

Se o seu computador **ainda não possui o JDK instalado**, acesse o site oficial da Oracle e baixe a versão mais recente do Java SE Development Kit (recomenda-se a versão 25 LTS).

👉 [Baixar o JDK — Oracle Java](https://www.oracle.com/br/java/technologies/downloads/)

### 🎓 Instalação passo a passo no Windows

Após o download, siga o tutorial abaixo, que explica **como instalar o JDK e configurar as variáveis JAVA_HOME e Path** de forma simples e visual:

👉 [Tutorial completo — Como instalar o JDK no Windows (YouTube)](https://www.youtube.com/watch?v=cT_VDy5TKTA)

> O vídeo mostra exatamente o processo que usamos neste projeto, incluindo a criação da variável de ambiente **JAVA_HOME** e a adição do caminho **bin** no **Path**, que são indispensáveis para que o VS Code reconheça o JDK corretamente.

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

> 💡 Se preferir, também é possível clicar em cada arquivo individualmente e selecionar **Instalar**.

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
| **Icon** | Deixe em branco | É opcional |
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

Com o perfil criado, o próximo passo é instalar as extensões que transformarão o VS Code em uma IDE completa para Java e Spring Boot.

#### 🔹 1. Extension Pack for Java  
👉 [Baixar no Marketplace](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-debug)

Este pacote oficial da **Microsoft e Red Hat** instala todas as ferramentas essenciais:
- **Language Support for Java™ (by Red Hat)** — suporte completo à linguagem Java.  
- **Debugger for Java** — depurador integrado.  
- **Test Runner for Java** — executa testes JUnit.  
- **Maven for Java** — integração com projetos Maven.  
- **Project Manager for Java** — gerencia dependências e estrutura do projeto.  
- **Visual Studio IntelliCode** *(opcional)* — sugestões inteligentes (pode desinstalar se quiser mais leveza).

> 💡 **Dica:** Após instalar o pack, o IntelliCode pode ser desinstalado sem afetar as demais extensões.

#### 🔹 2. Spring Boot Extension Pack  
👉 [Baixar no Marketplace](https://marketplace.visualstudio.com/items?itemName=vmware.vscode-boot-dev-pack)

Voltado para quem vai trabalhar com **Spring Boot**, o framework Java mais popular para back-end.  
Esse pacote instala automaticamente:
- **Spring Boot Dashboard** — gerencia e executa aplicações Spring direto do VS Code.  
- **Spring Boot Tools** — auxilia no desenvolvimento e debug.  
- **Spring Initializr Java Support** — cria novos projetos Spring Boot facilmente.

> 💡 Mesmo que você ainda não use o Spring, é interessante deixar o ambiente preparado.

#### 🔹 3. SonarQube for IDE (SonarLint)  
👉 [Baixar no Marketplace](https://marketplace.visualstudio.com/items?itemName=SonarSource.sonarlint-vscode)

O **SonarLint** analisa o código em tempo real e aponta problemas, más práticas e vulnerabilidades.  
É uma excelente ferramenta para quem quer escrever código limpo e profissional.

Principais funções:
- Análise estática local (sem precisar de servidor).  
- Sugestões de melhoria e correções automáticas (Quick Fix).  
- Pode ser conectado ao SonarQube Cloud para projetos em equipe.

> 💡 **Dica:** É como ter um mentor silencioso analisando seu código e te ensinando boas práticas.

#### 🔹 4. JetBrains Theme (opcional)  
👉 [Baixar no Marketplace](https://marketplace.visualstudio.com/items?itemName=kenethriera.jb-theme)

Tema escuro inspirado no IntelliJ IDEA, com contraste equilibrado e ótimo para longas sessões de trabalho.

#### 🔹 5. JetBrains Icon Theme (opcional)  
👉 [Baixar no Marketplace](https://marketplace.visualstudio.com/items?itemName=chadalen.vscode-jetbrains-icon-theme)

Adiciona ícones de pastas e arquivos no estilo JetBrains, deixando o ambiente mais agradável e organizado.

> 💡 Pronto! Seu VS Code estará visualmente idêntico ao IntelliJ IDEA, mas muito mais leve e rápido.

### 🪶 Resumo do passo 3

✅ Criamos um **Profile limpo** no VS Code;  
✅ Instalamos o **Extension Pack for Java**, o **Spring Boot Pack** e o **SonarLint**;  
✅ Aplicamos, opcionalmente, o **tema JetBrains** e os **ícones personalizados**;  

Com o ambiente configurado, o próximo passo será aplicar o **User Settings (JSON)** do projeto — onde ajustaremos o desempenho, a estética e o comportamento interno do VS Code.

---
