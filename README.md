## Como executar a Calculadora NIOSH

### 1. Pré-requisitos

- **Python 3.8 ou superior** instalado no computador ([baixar Python](https://www.python.org/downloads/))
- **Git** (opcional, apenas se quiser clonar o repositório pelo terminal)

### 2. Baixe o projeto

- Baixe o ZIP do repositório pelo GitHub e extraia, **ou** clone com:
   ```
   git clone https://github.com/seuusuario/seurepositorio.git
   ```

### 3. Instale as dependências

Abra o terminal/prompt de comando na pasta do projeto e execute:
```
pip install -r requirements.txt
```
Se for gerar o executável, instale também:
```
pip install pyinstaller
```

### 4. Execute a calculadora

Entre na pasta `src` e rode:
```
python app.py
```
O navegador abrirá automaticamente com a calculadora.

---

## Como gerar um executável (.exe) para Windows

1. No terminal, dentro da pasta `src`, rode:
    ```
    pyinstaller --onefile --add-data "calculadora.py;." app.py
    ```
2. O executável estará em `src/dist/app.exe`. Basta dar dois cliques para usar!

---

## Observações

- Se for compartilhar o executável, envie também a pasta `dist` gerada pelo PyInstaller.
- Para rodar em outro computador, pode ser necessário instalar o Visual C++ Redistributable (normalmente já vem no Windows).

# Calculadora NIOSH

## Descrição
Calculadora de levantamento de carga baseada na equação de NIOSH, desenvolvida em Python usando Gradio.

## Estrutura do Projeto
- `src/calculadora.py`: Funções de cálculo do RWL e LI.
- `src/app.py`: Interface visual com Gradio.
- `requirements.txt`: Bibliotecas necessárias.
- `assets/`: Recursos visuais opcionais.

## Como Executar
1. Clonar o repositório:
   ```bash
   git clone <URL_DO_REPOSITORIO>
   cd calculadora_niosh
   ```
2. Instalar dependências:
   ```bash
   pip install -r requirements.txt
   ```
3. Executar a aplicação:
   ```bash
   python src/app.py
   ```
4. A interface abrirá no navegador. Preencha os campos e clique em calcular.

## Como Empacotar em Executável (opcional)
1. Instale PyInstaller:
   ```bash
   pip install pyinstaller
   ```
2. Crie o executável:
   ```bash
   pyinstaller --onefile src/app.py
   ```
3. O executável será gerado na pasta `dist/`.

## Observações
- Preencha todos os campos obrigatórios: Peso Real, Distâncias, Altura, Ângulo, Frequência e Qualidade da Pegada.
- O resultado mostrará RWL (kg), LI e se o levantamento é seguro ou de risco.
