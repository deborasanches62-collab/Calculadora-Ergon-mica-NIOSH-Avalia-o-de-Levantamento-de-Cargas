
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
