# SCCCForge Pro (v1.0.0)

> **CCSDS 131.2-B-1 Flexible Advanced Coding and Modulation (SCCC) Space Telemetry Studio**  
> Complete 27-ModCod ACM Link Adapter, Physical Layer Frame (PLFRAME) Synthesizer, 320-Symbol Header Engine (256-Symbol Frame Marker \+ 64-Symbol Frame Descriptor), Distributed Pilot Pattern Distributor, Constellation I/Q Mapper, and 10-Point Normative Aerospace Standards Auditor.

---

## 🛰️ Product Overview

SCCCForge Pro is a specialized aerospace engineering tool engineered for Earth Observation (EO) satellite constellations, high-throughput science missions, and space telemetry ground stations. It provides reference software modeling, frame generation, link adaptation, and automated compliance auditing conforming strictly to **CCSDS 131.2-B-1** (*Flexible Advanced Coding and Modulation Scheme for High Rate Telemetry Applications*).

### Key Capabilities

- **Complete 27-ModCod Engine**: Covers all 27 normative CCSDS 131.2 formats across QPSK, 8PSK, 16APSK, 32APSK, and 64APSK modulations with code rates from 1/3 up to 26/27.  
- **320-Symbol PL Header Engine**: Generates 256-symbol Frame Marker (FM) Gold sequences and 64-symbol Frame Descriptor (FD) linear block codewords.  
- **Distributed Pilot Distributor**: Structures 240 pilot symbols across 15 subsections of 16 pilots each to enable robust carrier synchronization across nonlinear satellite TWTA amplifiers.  
- **Dynamic ACM Link Optimizer**: Analyzes operational link SNR (dB) and selects optimal ModCod providing maximum spectral efficiency while maintaining at least 0.5 dB Quasi-Error-Free (QEF) safety margin.  
- **Constellation I/Q Mapper**: Visualizes and calculates exact normalized constellation coordinates and ring radii ratios.  
- **10-Point Normative Standards Auditor**: Enforces rules SCCC-001 through SCCC-010 to verify mission readiness.  
- **Zero-Dependency Architecture**: Cross-platform pure ES6+ library, zero-dependency Python 3 CLI, and interactive HTML5 Mission Operations Console.

---

## 🚀 Quick Start

### 1\. Interactive Mission Operations Console

Open `source-code/index.html` in any web browser to test dynamic link SNR adaptation, inspect I/Q constellation diagrams, and run real-time compliance audits.

### 2\. Python Command Line Interface (CLI)

Synthesize a Physical Layer Frame (PLFRAME):

python3 source-code/sccc\_cli.py frame \--format 8

Select optimal ACM ModCod for a given link SNR:

python3 source-code/sccc\_cli.py acm \--snr 8.5

List all 27 normative ModCods with SNR thresholds:

python3 source-code/sccc\_cli.py modcods

Execute the 10-Point Normative Standards Audit:

python3 source-code/sccc\_cli.py audit \--format 8 \--snr 8.5

### 3\. Automated Test Suite

Run the 10 automated unit verification tests:

python3 source-code/test\_runner.py

---

## 📊 Compliance Matrix Summary

| Rule ID | Normative Checkpoint | Standard Reference | Status |
| :---: | :---- | :---- | :---: |
| **SCCC-001** | PL Header 320-Symbol Geometry | CCSDS 131.2-B-1 §5.2.1 | **PASS** |
| **SCCC-002** | Frame Marker Gold Sequence Sync | CCSDS 131.2-B-1 §5.2.2 | **PASS** |
| **SCCC-003** | Frame Descriptor 7-Bit Word Signaling | CCSDS 131.2-B-1 §5.2.3 | **PASS** |
| **SCCC-004** | FD Linear Block Code (64, 7\) Expansion | CCSDS 131.2-B-1 §5.2.4 | **PASS** |
| **SCCC-005** | 27 Normative ModCod Scheme Integrity | CCSDS 131.2-B-1 §4.2 | **PASS** |
| **SCCC-006** | Constellation Order & Bit-to-Symbol Mapping | CCSDS 131.2-B-1 §4.3 | **PASS** |
| **SCCC-007** | Distributed Pilot Pattern Geometry | CCSDS 131.2-B-1 §5.3 | **PASS** |
| **SCCC-008** | Pilot Symbol Amplitude Normalization | CCSDS 131.2-B-1 §5.3.2 | **PASS** |
| **SCCC-009** | Frame Scrambler Scrambling Exclusion | CCSDS 131.2-B-1 Annex C | **PASS** |
| **SCCC-010** | Quasi-Error-Free (QEF) SNR Link Budget Margin | CCSDS 131.2-B-1 Annex B | **PASS** |

---

## 💼 Commercial & Monetization Details

- **Target Customer**: Earth Observation (EO) satellite operators, space agency contractors, high-throughput satellite ground station developers, and CubeSat mission engineers.  
- **Distribution Model**: Professional Developer Seat & Enterprise Ground Station Site License.  
- **Pricing**: \$349/year per developer seat or \$2,499 one-time enterprise site license.  
- **Zero Cloud Infrastructure**: Client-side and local CLI execution with zero external data transmission.