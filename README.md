# Filtro Sobel — Detecção de Bordas

Desenvolvido por [RaffaellaSantos](https://github.com/RaffaellaSantos) e [oHenryy](https://github.com/oHenryy)

Descrição
-------

Este repositório contém um exercício/implementação do filtro Sobel, referente à disciplina de Tópicos Especiais para Computação I (Visão Computacional com Deep Learning), para detecção de bordas em imagens. O objetivo é demonstrar a aplicação do operador Sobel, comparar resultados, visualizar gradientes e experimentar com diferentes variantes (em CPU/PyTorch quando aplicável).

Conteúdo do repositório
-----------------------

- `Topicos1-2026.1-Tarefa1.ipynb`: Notebook com a implementação, exemplos, visualizações e explicações passo a passo.
- `requirements.txt`: Lista de dependências necessárias para reproduzir o ambiente.

Funcionalidades
--------------

- Aplicação do filtro Sobel para detecção de bordas (horizontal, vertical e magnitude).
- Visualização das imagens originais, gradientes e bordas resultantes.
- Código e experimentos organizados em notebook para fácil execução e modificação.

Requisitos
---------

Recomendado: Python 3.8 ou superior. Dependências listadas em `requirements.txt` (exemplo presente neste repositório):

```text
opencv-python
numpy
matplotlib
torch
torchvision
ipykernel
```

Instalação (ambiente virtual)
-----------------------------

1. Criar e ativar um ambiente virtual (Windows PowerShell):

```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
```

2. Atualizar pip e instalar dependências:

```powershell
python -m pip install --upgrade pip
pip install -r requirements.txt
```

Executando o notebook
---------------------

Inicie o Jupyter Notebook ou JupyterLab no diretório do projeto e abra `Topicos1-2026.1-Tarefa1.ipynb`:

```powershell
jupyter notebook
```

O notebook contém células com código e explicações; execute as células na ordem para reproduzir os resultados e visualizações.

Uso via script (exemplo)
-----------------------

Se desejar extrair trechos do notebook para um script Python, a lógica central do filtro Sobel pode ser aplicada com OpenCV/Numpy. Exemplo simples (em princípio encontrado no notebook):

```python
import cv2
import numpy as np

img = cv2.imread('exemplo.jpg', cv2.IMREAD_GRAYSCALE)
sobelx = cv2.Sobel(img, cv2.CV_64F, 1, 0, ksize=3)
sobely = cv2.Sobel(img, cv2.CV_64F, 0, 1, ksize=3)
magnitude = np.sqrt(sobelx**2 + sobely**2)
```