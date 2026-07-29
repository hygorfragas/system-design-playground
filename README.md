# System Design Playground 🎨

> **O simulador de infraestrutura e fluxo de carga interativo baseado em Blueprint para agentes de IA (Antigravity/Gemini).**

---

Sabe quando você tenta explicar a arquitetura de um sistema para alguém (especialmente iniciantes ou pessoas não-técnicas) e a pessoa começa a te olhar com aquela cara de *"tá falando grego"*? Ou quando você quer testar cenários de estresse no seu sistema mas não quer derrubar o ambiente? 

Esta skill resolve isso de um jeito **muito visual, interativo e direto ao ponto**!

## 🚀 O que ela faz?

Ela lê a estrutura do seu projeto atual ou a sua descrição de arquitetura e cria um **playground interativo local estilo blueprint** (uma grade azul clássica cheia de luzes e cabos que se mexem) rodando localmente no seu navegador.

Ao rodar a skill, ela analisa o projeto, gera o arquivo `system-design-canvas.html` na raiz do seu projeto e o **abre automaticamente no seu navegador padrão**.

---

## 🎮 Como funciona a interface interativa?

No arquivo HTML gerado, você ganha um painel operacional completo:
1. **Controle o tráfego**: Um controle deslizante (slider) no topo permite aumentar ou diminuir a quantidade de acessos por segundo (ex: de 100 a 5.000 req/s).
2. **Escale os recursos**: Botões de `+` e `-` nos cards dos componentes (App Server, Banco de Dados, Cache, Fila, Workers) permitem alterar as réplicas ativas em tempo real.
3. **Veja o gargalo acontecer**: À medida que o tráfego sobe ou você remove réplicas, as conexões mudam de cor (verde 🟢, laranja 🟡, vermelho 🔴) e aceleram a animação, mostrando exatamente onde a sobrecarga vai estourar primeiro.
4. **Painel de Dicas**: Um painel inteligente diz o que está quebrando e indica os arquivos e pastas do seu projeto que você precisa modificar para resolver.

---

## 🛠️ Como Instalar no seu Antigravity / Gemini

Para instalar esta custom skill no seu ambiente local, basta clonar este repositório ou copiar o arquivo `SKILL.md` para a pasta de custom skills da sua IA.

No macOS/Linux:
```bash
# Crie a pasta da skill caso não exista
mkdir -p ~/.gemini/config/skills/system-design-playground

# Copie o arquivo SKILL.md para lá
cp SKILL.md ~/.gemini/config/skills/system-design-playground/SKILL.md
```

### Como usar no chat:
Uma vez instalada, você pode invocar a skill digitando ou pedindo:
> *"Visualizar a arquitetura do projeto usando a skill System Design Playground"*

---

## 📄 Licença

Sinta-se livre para usar, melhorar e compartilhar! Distribuído sob a licença MIT.
