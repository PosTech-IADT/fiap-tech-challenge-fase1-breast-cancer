# Classificação de Câncer de Mama — FIAP Tech Challenge Fase 1

Este projeto utiliza aprendizado de máquina para classificar tumores de mama como benignos ou malignos. O notebook compara os modelos Gradient Boosting e Regressão Logística, com atenção especial ao recall da classe maligna.

## Estrutura principal

```text
.
├── Breast_Cancer.ipynb
├── data.csv
├── requirements.txt
└── README.md
```

- `Breast_Cancer.ipynb`: análise, preparação dos dados, treinamento e avaliação dos modelos.
- `data.csv`: conjunto de dados utilizado pelo notebook.
- `requirements.txt`: dependências Python necessárias para executar o projeto.

## Pré-requisitos

- Python 3.10 ou mais recente.
- Git para clonar o repositório.

Confirme se o Python está instalado:

```bash
python3 --version
```

No Windows, execute:

```powershell
python --version
```

## 1. Obter o projeto

Clone o repositório e acesse sua pasta:

```bash
git clone https://github.com/PosTech-IADT/fiap-tech-challenge-fase1-breast-cancer.git
cd fiap-tech-challenge-fase1-breast-cancer
```

Se o projeto já estiver no computador, abra o terminal diretamente na pasta que contém `Breast_Cancer.ipynb`.

## 2. Criar e ativar o ambiente virtual

### macOS ou Linux

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### Windows com PowerShell

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

### Windows com Prompt de Comando

```bat
python -m venv .venv
.venv\Scripts\activate.bat
```

Após a ativação, confirme que o interpretador pertence ao ambiente `.venv`:

```bash
python -c "import sys; print(sys.executable)"
```

O caminho exibido deve conter a pasta `.venv` do projeto.

## 3. Instalar as dependências

Com o ambiente virtual ativado, atualize o `pip` e instale os pacotes:

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

## 4. Executar o notebook

Ainda na raiz do projeto, inicie o JupyterLab:

```bash
jupyter lab Breast_Cancer.ipynb
```

O navegador abrirá o notebook. No JupyterLab, selecione o kernel Python pertencente ao ambiente `.venv`.

Execute as células em ordem por meio do menu **Run > Run All Cells**. O arquivo `data.csv` deve permanecer na mesma pasta do notebook, pois ele é carregado com um caminho relativo.

## Executar no Google Colab

1. Acesse [Google Colab](https://colab.research.google.com/).
2. Selecione **Arquivo > Fazer upload de notebook** e envie `Breast_Cancer.ipynb`.
3. Execute a primeira célula do notebook para instalar as bibliotecas necessárias:

   ```python
   %pip install -q pandas numpy matplotlib seaborn scikit-learn
   ```

4. No menu lateral esquerdo do Colab, abra **Arquivos**.
5. Clique em **Fazer upload para o armazenamento da sessão** e selecione `data.csv` neste repositório.
6. Confirme que o arquivo aparece no Colab como `/content/data.csv`. Não altere o nome do arquivo.
7. Execute as demais células em ordem por meio do menu **Ambiente de execução > Executar tudo**.

O armazenamento do Google Colab é temporário. Sempre que uma nova sessão for iniciada, envie novamente o arquivo `data.csv` antes de executar a célula que carrega o dataset.

## Encerrar o ambiente

Feche o JupyterLab com `Ctrl+C` no terminal e desative o ambiente virtual:

```bash
deactivate
```

## Principais bibliotecas

- `pandas`: leitura e tratamento dos dados.
- `numpy`: operações numéricas.
- `matplotlib` e `seaborn`: visualizações e matrizes de confusão.
- `scikit-learn`: pré-processamento, treinamento dos modelos e métricas.
- `jupyterlab` e `ipykernel`: execução interativa do notebook.

## Solução de problemas

- **`ModuleNotFoundError`**: confirme que o ambiente `.venv` está ativado e execute novamente `python -m pip install -r requirements.txt`.
- **`FileNotFoundError: data.csv`**: inicie o JupyterLab na raiz do projeto e confirme que `data.csv` está ao lado do notebook.
- **Kernel incorreto**: no JupyterLab, altere o kernel para o interpretador Python do ambiente `.venv`.
