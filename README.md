# Análise das Sete Emoções Básicas com DeepFace

## Descrição

Este projeto tem como objetivo analisar o reconhecimento de emoções faciais utilizando a biblioteca DeepFace, desenvolvida em Python. Foram utilizadas fotografias do próprio autor representando as sete emoções básicas para verificar a capacidade do modelo de Inteligência Artificial em identificar corretamente cada expressão facial.

O trabalho foi desenvolvido como atividade acadêmica da disciplina de Inteligência Artificial, utilizando o ambiente Google Colab para execução dos testes.

---

## Emoções Analisadas

As seguintes emoções foram avaliadas:

- Felicidade 
- Tristeza 
- Raiva 
- Medo 
- Surpresa 
- Nojo 
- Neutro 

---

## Tecnologias Utilizadas

- Python 3
- Google Colab
- OpenCV
- NumPy
- DeepFace

---

## Instalação

Instale a biblioteca DeepFace:

```bash
pip install deepface
````

Instale as dependências necessárias:

```bash
pip install opencv-python numpy
```

---

## Código Utilizado

```python
from google.colab import files

uploaded = files.upload()

import cv2
from deepface import DeepFace
from google.colab.patches import cv2_imshow

img = cv2.imread("IMG_00.jpg")

result = DeepFace.analyze(
    img,
    enforce_detection=False
)

print(result)

cv2_imshow(img)
```

---

## Metodologia

1. Foram capturadas fotografias representando cada uma das sete emoções.
2. As imagens foram enviadas para o Google Colab.
3. A biblioteca DeepFace realizou a detecção facial.
4. O modelo calculou a probabilidade de cada emoção.
5. Os resultados foram comparados com a emoção originalmente representada pelo autor.

---

## Resultados Obtidos

| Emoção Representada | Emoção Detectada | Resultado |
| ------------------- | ---------------- | --------- |
| Felicidade          | Happy            | ✅ Acerto  |
| Medo                | Happy            | ❌ Erro    |
| Surpresa            | Happy            | ❌ Erro    |
| Nojo                | Happy            | ❌ Erro    |
| Raiva               | Angry            | ✅ Acerto  |
| Neutro              | Neutral          | ✅ Acerto  |
| Tristeza            | Sad              | ✅ Acerto  |

### Taxa de Acerto

* Emoções analisadas: 7
* Emoções reconhecidas corretamente: 4
* Taxa de acerto: 57,14%

---

## Principais Observações

Os resultados demonstraram que o DeepFace apresentou bom desempenho na identificação das emoções de:

* Felicidade
* Raiva
* Tristeza
* Neutralidade

Por outro lado, o modelo apresentou dificuldades para reconhecer:

* Medo
* Surpresa
* Nojo

Essas emoções foram frequentemente classificadas como felicidade, demonstrando que sistemas de reconhecimento facial de emoções podem apresentar limitações dependendo da forma como a expressão é realizada.

---

## Estrutura do Projeto

```text
📁 Analise-Sete-Emocoes-DeepFace
│
├── README.md
├── analise_emocoes.ipynb
├── imagens/
│   ├── felicidade.jpg
│   ├── medo.jpg
│   ├── surpresa.jpg
│   ├── nojo.jpg
│   ├── raiva.jpg
│   ├── neutro.jpg
│   └── tristeza.jpg
│
└── relatorio.pdf
```

---

## Conclusão

O projeto permitiu avaliar o desempenho da biblioteca DeepFace no reconhecimento de emoções faciais. Os testes mostraram que a ferramenta possui boa capacidade para identificar algumas emoções, porém ainda apresenta limitações em expressões mais complexas, reforçando a necessidade de interpretação crítica dos resultados produzidos por sistemas de Inteligência Artificial.

---

## Autor

**Matheus Rodrigues Lima Ribeiro**

* Engenharia da Computação
* Python | Inteligência Artificial

Projeto acadêmico desenvolvido utilizando Python e DeepFace.

