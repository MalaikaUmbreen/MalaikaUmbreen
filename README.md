<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=28&duration=2800&pause=2000&color=00D9FF&center=true&vCenter=true&width=700&lines=Hi%2C+I'm+Malaika+Umbreen+%F0%9F%91%8B;Cybersecurity+Researcher+%F0%9F%94%90;SOC+Analyst+%7C+AI+for+Network+Defense+%F0%9F%A7%A0;Detecting+what+firewalls+cannot+see..." />

<br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=80&section=header&animation=twinkling" width="100%"/>

<br/>

![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)
![TryHackMe](https://img.shields.io/badge/TryHackMe-Active-red?style=for-the-badge&logo=tryhackme&logoColor=white)
![Views](https://komarev.com/ghpvc/?username=MalaikaUmbreen&style=for-the-badge&color=00d9ff&label=Profile+Views)

</div>

---

##                                     🔬 Featured Research - FYP Completed

<div align="center">

**A Transformer-based Detector for Network Steganography with Improved Generalization on unseen Covert Channels**  

</div>

> Network steganography hides malicious data inside normal DNS, ICMP, TCP, and UDP traffic — completely invisible to firewalls and IDS.  
> This research builds a Transformer-based detector that generalises to covert techniques it has **never seen before.**

---

##  Results vs Baselines

| Model | Accuracy | AUC-ROC | Gap |
|------|---------|--------|-----|
| 🏆 Our Transformer | 94.42% ±3.50% | 0.981 | — |
| LSTM | 78.40% ±6.20% | 0.871 | −16.02 pp |
| CNN | 76.20% ±5.80% | 0.854 | −18.22 pp |
| Random Forest | 69.80% ±8.10% | 0.802 | −24.62 pp |
| SVM | 63.10% ±9.40% | 0.743 | −31.32 pp |

**FPR:** 0.91% · **Protocol Attribution:** 94.30% · **Technique Classification:** 94.52% · **Model Size:** 6.9 MB  
All comparisons statistically significant — McNemar's test, p < 0.001

---

## 🏗️ Model Architecture

- **Input:** 225 flow-level behavioral features (each = 1 token)  
- **Encoder:** 4 Transformer blocks · 8-head attention  
- **FFN:** 128 → 256 → 128 (ReLU) · Dropout 0.30  

**Outputs:**
- Binary Detection (Sigmoid)
- Technique Classification (4-class Softmax)
- Protocol Attribution (4-class Softmax)

---

## 🧪 Feature Framework — 225 Features

| Category | Features | Detection |
|----------|--------|----------|
| Header Manipulation | 107 | TTL variance, TCP entropy |
| Timing Obfuscation | 50 | IAT patterns |
| Flow Blending | 73 | Packet rate, flow entropy |

---

## 📋 LOTO Evaluation — Unseen Techniques

| Split | Technique | Binary Acc | Protocol Acc | FPR |
|------|----------|-----------|-------------|-----|
| 1 | Timing | 90.60% | 92.84% | 0.90% |
| 2 | Flow | 99.05% | 91.15% | 1.18% |
| 3 | Header | 93.60% | 98.93% | 0.64% |
| **Mean** | All | **94.42%** | **94.30%** | **0.91%** |

---

## 🗃️ Dataset

- 13,848 labeled samples (DNS · ICMP · TCP · UDP)
- Tools: dns2tcp · dnscat2 · iodine · ptunnel · PingTunnel · cobalt strike  
- Behavioral training (no IPs, ports, timestamps)

---

## 🌐 Web Application + Agentic AI

| Feature | Description |
|--------|------------|
| 📤 Upload | PCAP / CSV |
| ⚡ Inference | 3.8ms/sample |
| 📊 Output | Binary + Technique + Protocol |
| 🗺️ Heatmaps | Attention visualization |
| 🤖 AI Agent | Writes SOC reports + explanations |

---

## 🛡️ SOC Journey

| Year | Milestone |
|-----|----------|
| 2025 | CTF + TryHackMe |
| 2025 | SOC Lab + Wazuh |
| 2025 | FYP Started |
| 2025 | 94.42% Accuracy |
| 2026 | AI Analyst Built |
| Now | Open to Roles  |

---

## 🧰 Tech Stack

### 🔐 Security
<p>
<img src="https://img.shields.io/badge/Kali_Linux-557C94?style=for-the-badge&logo=kali-linux"/>
<img src="https://img.shields.io/badge/Wireshark-1679A7?style=for-the-badge&logo=wireshark"/>
<img src="https://img.shields.io/badge/Nmap-4EAA25?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Metasploit-E34234?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Burp_Suite-FF6633?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Wazuh-005571?style=for-the-badge"/>
</p>

###                AI / ML
<p>
<img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge"/>
</p>

---

##               GitHub Stats

<div align="center">

<img height="160" src="https://github-readme-stats.vercel.app/api?username=MalaikaUmbreen&show_icons=true&theme=tokyonight&hide_border=true"/>
<img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=MalaikaUmbreen&layout=compact&theme=tokyonight&hide_border=true"/>

<br/>

<img src="https://streak-stats.demolab.com?user=MalaikaUmbreen&theme=tokyonight&hide_border=true"/>

<br/>

<img src="https://github-profile-trophy.vercel.app/?username=MalaikaUmbreen&theme=tokyonight&no-frame=true"/>

</div>

---

## 🤝 Let's Connect

Open to:
- SOC Analyst  
- Security Researcher  
- Junior Pentester  

![LinkedIn](https://img.shields.io/badge/LinkedIn-Malaika_Umbreen-0A66C2?style=for-the-badge&logo=linkedin)
![TryHackMe](https://img.shields.io/badge/TryHackMe-Malaika.Umbreen-212C42?style=for-the-badge&logo=tryhackme)

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=80&section=footer&animation=twinkling" width="100%"/>

**"Security is not a product, but a process." — Bruce Schneier**

</div>
