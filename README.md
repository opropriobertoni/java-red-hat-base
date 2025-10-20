# ☕ Java Red Hat Base — ambiente leve e otimizado para desenvolvimento Java no VS Code

**Um ambiente de desenvolvimento Java e Spring Boot completo, estável e otimizado para máquinas modestas com Sistema Operaciona Windows.** Criado com base na **Stack Red Hat**, este projeto busca oferecer uma alternativa **leve, limpa e eficiente** para quem deseja programar em Java usando o **Visual Studio Code**.

---

## 🧭 Sobre o projeto

Este repositório nasceu de um desafio pessoal: **criar um ambiente Java profissional e fluido em um notebook simples**, sem abrir mão das boas práticas de código, da estrutura moderna de desenvolvimento e do conforto visual.

Durante minha jornada de estudos em **backend com Java**, percebi que muitas configurações disponíveis na internet partem do pressuposto de que o desenvolvedor tem uma máquina robusta — o que não é a realidade de todos.  

Assim, comecei a construir o meu próprio ambiente: enxuto, rápido e organizado.  

O resultado é este projeto, que agora compartilho para ajudar outros desenvolvedores e estudantes que estão na mesma caminhada.

---

## 🎯 Objetivo

O propósito do **Java Red Hat Base** é entregar um ambiente pronto para trabalhar com **Java puro** e **Spring Boot**, sem precisar de configurações complexas.

Este setup foi pensado para quem quer:

✔️ Um **ambiente leve**, que roda bem até em notebooks básicos;  
✔️ Um **setup didático**, que explica cada ajuste e sua função;  
✔️ Uma **base confiável para estudos e projetos reais**;  
✔️ Um **padrão visual e de código consistente**, inspirado no ecossistema da JetBrains (IntelliJ IDEA).

---

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

---

## 📘 Estrutura do guia

O projeto foi dividido em **5 passos práticos e diretos**, para que você possa montar seu ambiente do zero com segurança:

✔️ **Configurando o ambiente Java**  
✔️ **Baixando e instalando a fonte JetBrains Mono**  
✔️ **Preparando o ambiente de desenvolvimento no VS Code**  
✔️ **Configurando o User Settings (arquivo JSON)**  
✔️ **Aplicando otimizações e dicas adicionais**

---

## ☕ 1° Passo — Instalando o JDK no Windows

Antes de começar a configurar o Visual Studio Code, é fundamental garantir que o **Java Development Kit (JDK)** esteja instalado corretamente no seu computador.

O **JDK** é o conjunto de ferramentas que permite **compilar, executar e depurar programas Java**. Sem ele, o VS Code não conseguirá reconhecer nem executar seu código Java.

---

### 🧩 Verificação prévia

Se você **já possui o JDK instalado** e **as variáveis de ambiente `JAVA_HOME` e `Path` configuradas corretamente**, pode **pular este passo** e seguir direto para a configuração do ambiente no VS Code.

> 💡 Para verificar, abra o **Terminal** (PowerShell ou Prompt de Comando) e digite:

> ```bash
> java -version
> echo %JAVA_HOME%
> ```
> Se ambos os comandos retornarem resultados válidos, o JDK está instalado e configurado corretamente.

---

### 📥 Download do JDK

Se o seu computador **ainda não possui o JDK instalado**, acesse o site oficial da Oracle e baixe a versão mais recente do Java SE Development Kit (recomenda-se a versão 25 LTS).

👉 [Baixar o JDK — Oracle Java](https://www.oracle.com/br/java/technologies/downloads/)

---

### 🎓 Instalação Passo a Passo no Windows

Após o download, siga o tutorial abaixo, que explica **como instalar o JDK e configurar as variáveis JAVA_HOME e Path** de forma simples e visual:

🎥 [Tutorial completo — Como instalar o JDK no Windows (YouTube)](https://www.youtube.com/watch?v=cT_VDy5TKTA)

> O vídeo mostra exatamente o processo que usamos neste projeto, incluindo a criação da variável de ambiente **JAVA_HOME** e a adição do caminho **bin** no **Path**, que são indispensáveis para que o VS Code reconheça o JDK corretamente.

---

