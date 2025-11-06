# Rossmann_Store_Sales

## Instalação das Dependências

### Pré-requisitos

No macOS, é necessário instalar o OpenMP runtime antes de instalar o XGBoost:

```bash
brew install libomp
```

### Instalação das Bibliotecas Python

1. Ative o ambiente virtual (se estiver usando pyenv):

```bash
pyenv activate Rossman
```

Ou se estiver usando outro gerenciador de ambiente virtual:

```bash
source venv/bin/activate  # ou o caminho do seu ambiente virtual
```

2. Instale as dependências:

```bash
pip install -r requirements.txt
```

Se o XGBoost ainda apresentar problemas após instalar o libomp, reinstale-o:

```bash
pip install --force-reinstall xgboost
```

### Solução de Problemas

Se encontrar o erro `XGBoostError: XGBoost Library (libxgboost.dylib) could not be loaded`:

1. Certifique-se de que o libomp está instalado: `brew list libomp`
2. Reinstale o XGBoost: `pip install --force-reinstall xgboost`
3. Reinicie o kernel do Jupyter Notebook