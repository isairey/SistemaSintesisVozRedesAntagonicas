<div align="center">

<img width="220" src="https://cdn-icons-png.flaticon.com/512/3659/3659898.png" />

# 🎙️ SistemaSintesisVozRedesAntagonicas

### Generative Adversarial Networks para síntesis de voz de alta fidelidad 🚀

<p align="center">
  <b>SistemaSintesisVozRedesAntagonicas</b> es un vocoder basado en GANs capaz de generar audio de alta calidad a partir de espectrogramas Mel con una velocidad muy superior al tiempo real.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/HiFi--GAN-SpeechSynthesis-blueviolet?style=for-the-badge">
  <img src="https://img.shields.io/badge/PyTorch-DeepLearning-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white">
  <img src="https://img.shields.io/badge/GAN-AudioGeneration-purple?style=for-the-badge">
  <img src="https://img.shields.io/badge/AI-VoiceSynthesis-00C853?style=for-the-badge">
</p>

<p align="center">
  <a href="#-acerca-del-proyecto">Acerca</a> •
  <a href="#-características">Características</a> •
  <a href="#-tecnologías-utilizadas">Tecnologías</a> •
  <a href="#-instalación">Instalación</a> •
  <a href="#-entrenamiento">Entrenamiento</a>
</p>

</div>

---

# 🌌 Acerca del proyecto

**SistemaSintesisVozRedesAntagonicas (High Fidelity GAN)** es un modelo de síntesis de voz basado en Redes Generativas Antagónicas (GANs) diseñado para convertir espectrogramas Mel en audio de alta calidad.

El proyecto destaca por:

* 🎙️ Síntesis de voz natural
* ⚡ Generación extremadamente rápida
* 🧠 Arquitectura basada en GAN
* 🎵 Audio de alta fidelidad
* 🚀 Inferencia en tiempo real
* 💾 Bajo consumo de recursos

---

# ✨ Características

## 🎤 Síntesis de Voz

* Conversión Mel → Audio
* Calidad cercana a voz humana
* Compatibilidad con múltiples datasets
* Soporte para múltiples hablantes

---

## ⚡ Alto Rendimiento

* Generación en tiempo real
* Inferencia optimizada
* Compatible con GPU y CPU
* Baja latencia

---

## 🧠 Deep Learning

* Arquitectura GAN
* Generadores optimizados
* Discriminadores multi-período
* Discriminadores multi-escala

---

## 🔄 Integración

* Compatible con Tacotron2
* Compatible con Glow-TTS
* Compatible con sistemas TTS personalizados
* Fine-tuning sencillo

---

# 👨‍💻 Arquitectura del sistema

## 🎙️ Generator

Módulo encargado de generar la señal de audio.

### Funcionalidades

* Conversión Mel-Spectrogram → Waveform
* Generación eficiente
* Audio de alta calidad
* Inferencia rápida

---

## 🎧 Multi-Period Discriminator

Analiza patrones periódicos de la voz.

### Funcionalidades

* Captura características temporales
* Mejora calidad del audio
* Reduce artefactos

---

## 📊 Multi-Scale Discriminator

Evalúa la señal en diferentes escalas.

### Funcionalidades

* Mayor realismo
* Estabilidad durante entrenamiento
* Calidad perceptual mejorada

---

# 🛠️ Tecnologías utilizadas

## 🧠 Inteligencia Artificial

<p>
  <img src="https://skillicons.dev/icons?i=python,pytorch" />
</p>

* Python
* PyTorch
* GANs
* Deep Learning

---

## 🎙️ Procesamiento de Audio

<p>
  <img src="https://skillicons.dev/icons?i=python" />
</p>

* Mel Spectrograms
* Speech Processing
* Audio Synthesis
* Neural Vocoder

---

## 🧰 Herramientas

<p>
  <img src="https://skillicons.dev/icons?i=git,github,vscode,linux" />
</p>

* Git
* GitHub
* VS Code
* Linux

---

# 📂 Estructura del proyecto

```bash
SistemaSintesisVozRedesAntagonicas/
│
├── configs/
├── checkpoints/
├── generated_files/
├── generated_files_from_mel/
├── test_files/
├── test_mel_files/
├── train.py
├── inference.py
├── inference_e2e.py
├── meldataset.py
├── models.py
├── requirements.txt
└── README.md
```

---

# ⚡ Instalación

## 📋 Requisitos

* Python 3.6+
* PyTorch
* CUDA (Opcional)
* Git
* Dataset LJSpeech

---

# 🚀 Configuración del proyecto

## 1️⃣ Clonar repositorio

```bash
git clone https://github.com/isairey/SistemaSintesisVozRedesAntagonicas.git
```

---

## 2️⃣ Entrar al proyecto

```bash
cd SistemaSintesisVozRedesAntagonicas
```

---

## 3️⃣ Instalar dependencias

```bash
pip install -r requirements.txt
```

---

## 4️⃣ Descargar dataset

Descargar:

```text
LJSpeech Dataset
```

y mover los archivos WAV a:

```bash
LJSpeech-1.1/wavs
```

---

# 🎯 Entrenamiento

## Modelo V1

```bash
python train.py --config config_v1.json
```

---

## Modelo V2

```bash
python train.py --config config_v2.json
```

---

## Modelo V3

```bash
python train.py --config config_v3.json
```

---

# 📊 Modelos preentrenados

HiFi-GAN proporciona modelos listos para usar:

| Modelo       | Dataset   |
| ------------ | --------- |
| LJ_V1        | LJSpeech  |
| LJ_V2        | LJSpeech  |
| LJ_V3        | LJSpeech  |
| VCTK_V1      | VCTK      |
| VCTK_V2      | VCTK      |
| VCTK_V3      | VCTK      |
| UNIVERSAL_V1 | Universal |

---

# 🔥 Fine-Tuning

HiFi-GAN permite ajustar modelos ya entrenados utilizando espectrogramas generados por otros sistemas TTS.

### Compatibilidad

* Tacotron2
* Glow-TTS
* FastSpeech
* Modelos personalizados

Ejemplo:

```bash
python train.py --fine_tuning True --config config_v1.json
```

---

# 🎧 Inferencia desde archivos WAV

## Preparar archivos

Crear:

```bash
test_files/
```

y copiar los audios WAV.

---

## Ejecutar inferencia

```bash
python inference.py \
--checkpoint_file checkpoint.pt
```

Los resultados se almacenarán en:

```bash
generated_files/
```

---

# 🎙️ Inferencia End-to-End

Generar audio directamente desde espectrogramas Mel.

```bash
python inference_e2e.py \
--checkpoint_file checkpoint.pt
```

Los resultados se almacenarán en:

```bash
generated_files_from_mel/
```

---

# 📡 Casos de uso

## 🗣️ Síntesis de voz

* Asistentes virtuales
* Lectores automáticos
* Sistemas conversacionales
* Audiolibros

---

## 🤖 Inteligencia Artificial

* TTS Neural
* Voice Cloning
* Generación de voz
* Aplicaciones multimodales

---

## 🎓 Investigación

* Procesamiento de voz
* Deep Learning
* Generative Models
* GAN Research

---

# 🧠 Objetivos del proyecto

## 🚀 Optimización de TTS

* Generación rápida
* Audio realista
* Escalabilidad
* Calidad cercana a voz humana

---

## 📖 Investigación

* Arquitecturas GAN
* Síntesis neural
* Aprendizaje profundo
* Procesamiento de señales

---

# 🚧 Roadmap

## 🔮 Próximas mejoras

* Modelos más compactos
* Mejor rendimiento CPU
* Soporte multilingüe
* Integración con LLMs
* Optimización para Edge Devices

---

# 🤝 Contribuciones

Las contribuciones son bienvenidas ❤️

## Cómo contribuir

1. Fork del proyecto

```bash
git checkout -b feature/nueva-funcionalidad
```

2. Commit

```bash
git commit -m "✨ Nueva funcionalidad"
```

3. Push

```bash
git push origin feature/nueva-funcionalidad
```

4. Pull Request 🚀

---

# 👨‍💻 Desarrollador
<div align="center">

## Isai Reyes - FullStack Developer



</div>

---

# 🌟 Apoya el proyecto

⭐ Dale una estrella
🍴 Haz fork
📢 Comparte el proyecto

---

# 📜 Licencia

Proyecto open source orientado a investigación, desarrollo y aplicaciones avanzadas de síntesis de voz mediante Deep Learning.

---

<div align="center">

### 🎙️ SistemaSintesisVozRedesAntagonicas — generación de voz de alta fidelidad impulsada por Inteligencia Artificial 🚀

</div>
