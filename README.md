# 🧠 When Quantum States Learn: Fidelity as the Heart of Quantum Machine Learning  

This project explores how **quantum fidelity** — the overlap between two quantum states — can be used as a foundation for **Quantum Machine Learning (QML)**.  
Built entirely with **Qiskit** and **scikit-learn**, it demonstrates a **SWAP-test-based quantum kernel** and studies how **noise** affects quantum learning performance.

---

## 🚀 Overview  

We designed a **quantum kernel SVM** that classifies 3D classical data encoded into quantum states.  
The **SWAP test** computes fidelity between each pair of states, creating a **quantum kernel matrix** that serves as the basis for learning.  
To simulate realistic quantum devices, we added **noise models** (depolarizing, amplitude damping, and readout errors) and analyzed how they degrade classification accuracy and fidelity structure.  

---

## ⚙️ Key Components  

### 1. **Quantum Feature Encoding**
- 3D classical features → quantum rotations on Bloch sphere (`RY` and `RZ` gates)
- Each data point encoded into a single-qubit quantum state

### 2. **Fidelity Measurement via SWAP Test**
- Computes `|⟨ψ_i | ψ_j⟩|²` between two quantum states  
- Used to build the **quantum kernel matrix**

### 3. **Noise Models**
- **Depolarizing noise:** randomizes qubit state  
- **Amplitude damping:** simulates energy loss  
- **Readout error:** introduces measurement inaccuracy  

### 4. **Learning Model**
- Quantum kernel used in **SVM (Support Vector Machine)** classifier
- Compared clean vs noisy accuracy (~1.0 → ~0.68)

### 5. **Visualizations**
- Bloch sphere representation of encoded states  
- 3D scatter plots of classification results  
- Heatmaps showing kernel similarity structure under noise  

---

## 📊 Results  

| Setup | Description | Accuracy |
|--------|--------------|-----------|
| Ideal (No Noise) | Perfect fidelity between same-class states | ~1.00 |
| Moderate Noise | Small decoherence and overlap blur | ~0.80 |
| High Noise | Significant degradation in fidelity and separability | ~0.68 |

🧩 **Observation:**  
Quantum fidelity captures similarity effectively, but is sensitive to decoherence.  
Even under noise, the model retained partial separability — highlighting potential for **noise-resilient quantum ML**.

---

## 🧰 Requirements  

