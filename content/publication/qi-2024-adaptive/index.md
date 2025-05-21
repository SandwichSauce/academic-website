---
title: Adaptive brain-computer interface decoding method based on multi-model dynamic
  integration
authors:
- Yu Qi
- Yueming Wang
- admin
- Kedi Xu
- Gang Pan
date: '2024-10-01'
publishDate: '2025-05-20T09:55:05.134400Z'
publication_types:
- patent

publication: '*PATENT COOPERATION TREATY*'
publication_short: 'PCT'
---
# 🧠 Intracortical Brain-Computer Interfaces and Neural Decoding

## 📌 Overview

**Brain-Computer Interfaces (BCIs)** enable the **direct decoding of motion intentions** from neural activity for external control.  
Among them, **intracortical BCIs**—which use **implanted electrode arrays**—have notably advanced applications such as:

- 🦾 **Exoskeleton control**
- 🖱️ **Computer cursor navigation**

---

## 🧩 Role of Neural Decoding Algorithms

Neural decoding algorithms are **central to intracortical BCI systems**.  
They translate neural activity into meaningful control signals using methods like:

- 📈 **Population Vector Methods**
- 📊 **Optimal Linear Estimation (OLE)**
- 🤖 **Deep Neural Networks**
- 🔁 **Recursive Bayesian Decoders**

> ✅ Among these, the **Kalman Filter** is the **most widely used** in **online cursor and exoskeleton control**, as it incorporates motion dynamics as **prior knowledge**, leading to **state-of-the-art performance**.

---

## 🇨🇳 Example: EEG-Based BCI System (Patent CN107669416A)

A notable real-world implementation is documented in **Chinese Patent CN107669416A**, describing a **motor imagery-based EEG wheelchair control system**.

### 🧩 System Components

- 🧠 EEG signal acquisition system  
- 🧠 Decoding device with:
  - **Continuous motor imagery module**
  - **Brisk motor imagery module**
- 🦽 Electric wheelchair

> Each module targets a specific EEG pattern, enhancing **responsiveness** and **system flexibility**.

---

## ⚠️ Challenge: Neural Signal Instability

Despite progress, **neural decoding still suffers from instability**, particularly over long durations.

### 🔍 Causes of Instability

- 🔊 **Neuronal noise**
- ❌ **Signal dropout**
- 🔄 **Plasticity and shifting brain states**

> ⚠️ These factors **alter the neural-to-kinematic mapping** over time, making **static decoding models ineffective** in long-term use.

### 📉 Consequences

- **Performance degrades** over time  
- **Frequent retraining** of models is required

---

## 🧠 Decoder Strategies for Neural Variability

### 1. 🔁 Fixed Models + Recalibration

- Use **periodic retraining** or **incremental updates**
- ✅ Pros: Simplicity, widely tested
- ❌ Cons: Labor-intensive, poor adaptability

### 2. 📡 Dynamic Models

- **Track and adapt** to neural signal changes
- Offer potential for **long-term robustness**
- 🚧 Still underexplored, especially for **direct modeling of unstable signals**

---

## ❓ Research Problem

> 🧠 **Key Question**:  
How can we design **dynamic neural decoders** that effectively model **unstable neural signals** and provide **robust motor decoding** over time?

This represents a **pressing challenge** for developing **reliable, long-term intracortical BCI systems**.
