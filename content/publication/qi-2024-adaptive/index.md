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
# Intracortical Brain-Computer Interfaces and Neural Decoding

## Overview

Brain-computer interfaces (BCIs) enable **direct decoding of motion intentions** from neural signals for external device control.  
**Intracortical BCIs**, which utilize implanted electrode arrays, have greatly advanced the development of:
- **Exoskeleton devices**
- **Computer cursor control**

## Role of Neural Decoding Algorithms

Neural decoding algorithms are **central to intracortical BCI systems**.  
Various algorithms have been proposed to extract motion-related information, including:

- **Population Vector Methods**
- **Optimal Linear Estimation (OLE)**
- **Deep Neural Networks**
- **Recursive Bayesian Decoders**

> ✅ Among these, the **Kalman Filter** is widely used in **online cursor and exoskeleton control** due to its integration of motion dynamics as prior knowledge, achieving the best performance so far.

## Example: EEG-Based BCI System (Chinese Patent: CN107669416A)

A representative application is disclosed in **Chinese patent CN107669416A**, which describes a **wheelchair system** based on **motor imagery EEG decoding**.  
System components include:
- EEG signal acquisition system
- Decoding device (with continuous and brisk motor imagery decoding modules)
- Electric wheelchair

Each decoding module processes a specific type of EEG signal, enhancing system responsiveness and flexibility.

## Challenge: Neural Signal Unstability

Despite advancements, **signal instability** remains a major challenge in neural decoding.

### Causes of Instability

- **Neuronal noise**
- **Neuronal signal dropout**
- **Neuronal plasticity and changing brain states**

> ⚠️ As a result, the **neural signal-to-kinematic mapping** may change over time, making **fixed decoding models unreliable** during long-term usage.

### Consequences

- Decoding accuracy **degrades over time**
- Fixed models must be **frequently retrained**

## Decoder Categories: Coping with Neural Variability

### 1. Fixed Models with Recalibration

- Most common approach
- Rely on **periodic retraining** or **incremental parameter updates**
- **Pros**: Simple, proven
- **Cons**: High cost of retraining, poor adaptability

### 2. Dynamic Models for Signal Tracking

- **Adaptively track changes** in neural signals
- Better suited for **long-term decoding**
- Still **underexplored**, especially in directly modeling **unstable signals**

## Research Problem

> 🧠 **Key Open Question**:  
How can we use **dynamic models** to effectively model **unstable neural signals** and achieve **robust decoding performance** in motor neural decoding?

This is a **pressing challenge** in the development of reliable and long-lasting motor decoding systems in BCIs.
