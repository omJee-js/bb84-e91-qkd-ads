# Hardware-Aware Quantum Key Distribution (QKD) Simulation

Simulation of BB84 and E91 quantum key distribution protocols under realistic hardware noise conditions using Qiskit.

This project evaluates quantum bit error rate (QBER) and secure key generation in the presence of hardware-constrained, non-ideal effects such as decoherence and readout errors. Hardware parameters are derived from electromagnetic and pulse-level simulations in Keysight ADS.

---

## Protocols Implemented

### BB84 (Prepare-and-Measure)
- Random bit and basis generation
- Basis reconciliation and key sifting
- Quantum Bit Error Rate (QBER) calculation
- Security validation of the generated key

### E91 (Entanglement-Based)
- Bell-pair (entangled qubit) generation
- Random basis measurement by two parties
- Correlation-based key extraction
- QBER calculation and secure key validation

---

## Hardware Noise Model
- **Depolarizing noise:** modeled from gate fidelity  
- **Amplitude damping:** based on T1 relaxation times  
- **Measurement readout error:** simulates imperfect qubit measurement  

These noise effects are incorporated using **Qiskit Aer’s NoiseModel** to simulate realistic quantum hardware behavior.

---

## Technologies Used
- Python 3.9+
- Qiskit
- Qiskit Aer
- NumPy
- Keysight ADS (for hardware parameter extraction)

---

## Installation

1. Clone the repository:
```bash
git clone <repository_url>
cd <repository_folder>
2. Install dependencies:
```bash
pip install qiskit qiskit-aer numpy

Expected Outputs
Quantum Bit Error Rate (QBER)
Secure key generation rate
Correlation plots for E91 (if implemented)
Console logs showing protocol steps


├── README.md
├── bb84_simulation.py
├── e91_simulation.py
├── requirements.txt
└── utils/
    └── noise_models.py



References

Bennett, C. H., & Brassard, G. (1984). Quantum cryptography: Public key distribution and coin tossing.

Ekert, A. K. (1991). Quantum cryptography based on Bell’s theorem.