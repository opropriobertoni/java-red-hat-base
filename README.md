# ☕ Java Red Hat Base — VS Code Environment

> Ambiente Java + Spring Boot no VS Code, **otimizado para máquinas modestas**, com Stack Microsoft/Red Hat, SonarQube for IDE e tema/ícones JetBrains.
> Portabilidade total via **JAVA_HOME** (sem caminhos fixos no JSON).

---

## 🚀 Como usar

1) **Defina o JAVA_HOME (Windows PowerShell):**
```powershell
setx JAVA_HOME "C:\Program Files\Java\jdk-25"
setx PATH "%JAVA_HOME%\bin;%PATH%"
```
Feche e reabra o VS Code/terminal, depois confirme:
```powershell
java -version
```

2) **Importe o perfil**
- VS Code → **File → Preferences → Profiles → Import Profile...**
- Escolha: `java-red-hat-base-full.code-profile`
- Aceite instalar as extensões recomendadas.

3) **(Opcional) Abra a pasta do repo**
Se você abrir só a pasta, as recomendações do VS Code vêm de `.vscode/extensions.json`.

---

## 📦 Inclui

- **Extension Pack for Java** (Microsoft/Red Hat)
- **Spring Initializr / Boot Tools / Boot Dashboard**
- **SonarQube for IDE** (modo leve: onSave)
- **JetBrains Dark Theme + Icon Theme**
- **Google Java Style** (format on save)

---

## 🧠 Por que JAVA_HOME?

- Funciona em **qualquer SO** (Windows/Linux/macOS).
- VS Code, Maven, Gradle, Spring e outras ferramentas já reconhecem.
- Para atualizar o JDK, basta mudar o `JAVA_HOME` — **zero edição no JSON**.

---

## 🧩 Estrutura sugerida do repositório

```
java-red-hat-base/
├─ java-red-hat-base-full.code-profile   # Perfil importável (instala extensões)
├─ java-red-hat-base.jsonc               # Settings com comentários (JSONC)
├─ .vscode/
│  └─ extensions.json                    # Recomendações de extensões
└─ README.md
```

---

## 🔎 Dicas de performance (notebooks modestos)

- `"editor.minimap.enabled": false`
- `"sonarlint.analyzer.runMode": "onSave"`
- `"terminal.integrated.gpuAcceleration": "auto"` (troque para `"off"` se notar flicker)

---

## 👤 Autor

**Daniel César Bertoni de Oliveira** — ambiente público e didático para acelerar seu setup Java no VS Code.
