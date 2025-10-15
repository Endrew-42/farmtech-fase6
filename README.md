# 🧠 FASE 6 – O COMEÇO DA REDE NEURAL  
## Projeto: FarmTech Solutions – Sistema de Visão Computacional com YOLO  

---

### 👥 Integrantes  

| Nome | RM | E-mail |
|------|----|---------|
| **Endrew Alves dos Santos** | RM563646 | Endrewalves42@gmail.com |
| **João Vittor Fontes** | RM565999 | fontesjoaovittor@gmail.com |
| **Vinicius Divino** | RM566269 | nisoxds@gmail.com |
| **Tayna Esteves** | RM562491 | esteves.tayna96@gmail.com |
| **Carlos Souza** | RM566487 | carlos.souza004@gmail.com |

---

## 🚀 Descrição do Projeto

A **FarmTech Solutions**, empresa originalmente voltada ao agronegócio, está expandindo suas soluções de **Inteligência Artificial** para novas áreas, como **segurança patrimonial, saúde animal e visão computacional**.

O objetivo deste projeto foi **demonstrar na prática o potencial de sistemas de visão computacional**, desenvolvendo e comparando diferentes abordagens de redes neurais para **detecção e classificação de imagens** utilizando o **YOLO (You Only Look Once)** e uma **CNN desenvolvida do zero**.

---

## 📸 Etapa 1 – Dataset e Rotulação

O grupo construiu um **dataset personalizado** contendo imagens de dois objetos distintos: **caneca** e **pote**.  
As imagens foram capturadas manualmente e rotuladas usando a plataforma [Make Sense AI](https://www.makesense.ai).

📦 **Dataset organizado no Google Drive:**  
[Link do dataset](https://drive.google.com/drive/folders/12sngRVFVBz5B0g77vGanBMX9hWxbNTSg?usp=drive_link)

**Estrutura do dataset:**
```
/dataset
 ├── /train
 │    ├── /caneca/
 │    └── /pote/
 ├── ROTULACAO DAS IMAGENS YOLO_readme.docx
 └── Make Sense - Google Chrome 2025-10-12.mp4
```

As anotações seguem o padrão YOLO:
```
<class_id> <x_center> <y_center> <width> <height>
```
- `class_id = 0` → caneca  
- `class_id = 1` → pote  

---

## ⚙️ Etapa 2 – Modelos Treinados

O projeto comparou **três abordagens principais** para classificação e detecção dos objetos.

### 🧩 1. YOLO Customizado
- Modelo treinado com base em dataset próprio.  
- Duas execuções: 30 e 60 épocas.  
- Resultados salvos em `runs/detect/expX`.  
- Apresentou a **maior precisão geral** entre os modelos.  

### 🧠 2. YOLO Tradicional
- Implementação base do YOLOv5 com parâmetros padrão.  
- Serviu de referência para avaliar a influência da customização.  
- Teve **bons resultados**, mas confundiu o fundo em alguns casos.  

### 🔬 3. CNN do Zero
- Rede neural criada e treinada em **TensorFlow/Keras**.  
- Dataset balanceado com 8 imagens de teste (4 de cada classe).  
- Acurácia de **100%**, porém indicando possível **overfitting** devido ao tamanho reduzido da base.  

---

## 📊 Resultados e Comparações  

| Modelo | Acurácia / Precisão | Tempo de Treinamento | Facilidade de Integração | Observações |
|---------|---------------------|----------------------|---------------------------|--------------|
| YOLO Customizado | **93% (mAP@50)** | Médio | Alta | Melhor desempenho geral |
| YOLO Tradicional | **88% (mAP@50)** | Rápido | Alta | Pequenas confusões com fundo |
| CNN do Zero | **100% (8 imagens de teste)** | Longo | Média | Dataset pequeno → possível overfitting |

**Matrizes de confusão:**
- CNN do Zero: 8 acertos em 8 imagens (4 canecas + 4 potes).  
- YOLO Customizado e Tradicional: ambas distinguiram com precisão, mas a versão customizada teve melhor mAP.  

---

## 🎥 Demonstração em Vídeo

Assista à execução prática do projeto e aos resultados visuais do modelo YOLO:

📺 **[Link do vídeo no YouTube – Não listado]**  
👉 *[adicione aqui o link do vídeo quando o upload estiver concluído.](https://www.youtube.com/watch?v=78cHdVs-CEU)*

---

## 🧩 Conclusões

- O modelo **YOLO Customizado** apresentou o melhor equilíbrio entre **velocidade e precisão**, demonstrando excelente aplicabilidade prática.  
- O **YOLO Tradicional** também teve bom desempenho, mas com menor precisão em cenários de fundo complexo.  
- A **CNN do Zero** atingiu acurácia perfeita no teste, porém isso se deve ao baixo volume de dados e menor generalização.  

**Conclusão geral:**  
> Modelos pré-treinados e customizados, como o YOLOv5, são mais eficientes e escaláveis para detecção de objetos em aplicações reais da FarmTech Solutions.

---

## 🧰 Tecnologias Utilizadas

- Python 3.x  
- Google Colab  
- YOLOv5 (Ultralytics)  
- TensorFlow / Keras  
- OpenCV  
- Make Sense AI  
- NumPy, Pandas, Matplotlib  

---

## 📚 Referências  

- FIAP – Capítulo 3: *Redes Neurais e YOLO*  
- Ultralytics YOLOv5 Documentation  
- TensorFlow Keras API  
- MakeSense.AI Labeling Tool  
- [YOLOv5 GitHub Repository](https://github.com/ultralytics/yolov5)

---
