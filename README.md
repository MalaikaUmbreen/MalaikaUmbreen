<div align="center">
<!-- Animated typing header -->
<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=32&duration=2800&pause=2000&color=00D9FF&center=true&vCenter=true&width=700&lines=Hi%2C+I'm+Malaika+Umbreen+%F0%9F%91%8B;Cybersecurity+Researcher;SOC+Analyst+%7C+AI+for+Network+Defense;Building+the+Future+of+Threat+Detection" alt="Typing SVG" />
<br/>
<!-- Animated wave banner -->
<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,50:00D9FF,100:7C3AED&height=120&section=header&animation=fadeIn"/>
`Cybersecurity Researcher` · `SOC Analyst` · `AI for Network Defense`
Detecting what others cannot see — covert channels in network traffic
<br/>
![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)
![TryHackMe](https://img.shields.io/badge/TryHackMe-Profile-212C42?style=for-the-badge&logo=tryhackme&logoColor=red)
![Profile Views](https://komarev.com/ghpvc/?username=MalaikaUmbreen&style=for-the-badge&color=00d9ff&label=Profile+Views)
</div>
---
🔬 Featured Research — Final Year Project (Completed ✅)
<div align="center">
`A Transformer-based Detector for Network Steganography with Improved Generalization`
Air University, Islamabad · Department of Cybersecurity
Supervisor: Dr. Zunera Jalil
</div>
> *Network steganography is one of the most operationally dangerous anti-forensic threats in cybersecurity — hiding malicious communication inside normal DNS, ICMP, TCP, and UDP traffic, completely invisible to firewalls and IDS. This research applies a Transformer architecture to detect it with generalization existing models cannot achieve.*
📊 Key Results
Metric	Our Transformer	Best Baseline (LSTM)
Mean Binary Detection Accuracy	94.42% ±3.50%	78.40% ±6.20%
Protocol Attribution Accuracy	94.30%	—
Technique Classification Accuracy	94.52%	—
AUC-ROC	0.981	0.871
False Positive Rate	0.91%	—
Margin over LSTM	+16.02 pp	baseline
Margin over CNN	+18.22 pp	—
Margin over Random Forest	+24.62 pp	—
Model Size	6.9 MB	3.4 MB
All pairwise comparisons statistically significant — McNemar's test, p < 0.001
🏗️ Architecture
```
INPUT: 225 Flow-Level Behavioral Features per network flow
       ↓
Each feature treated as an independent attention TOKEN (seq. length = 225)
       ↓
┌─────────────────────────────────────────────────────┐
│         TRANSFORMER ENCODER STACK (4 blocks)        │
│  • 8-Head Self-Attention (16-dim subspaces/head)    │
│  • Feedforward: 128 → 256 → 128 (ReLU)             │
│  • Residual connections + Layer Normalization       │
│  • Dropout: 0.30  |  Embedding dim: 128             │
└─────────────────────────────────────────────────────┘
       ↓ Global Average Pooling
┌──────────────┬──────────────────┬──────────────────┐
│  HEAD 1      │  HEAD 2          │  HEAD 3          │
│  Binary      │  Technique       │  Protocol        │
│  Detection   │  Classification  │  Attribution     │
│  Normal vs.  │  Header Manip /  │  DNS / ICMP /    │
│  Covert      │  Timing Obfusc / │  TCP / UDP       │
│  (Sigmoid)   │  Flow Blending   │  (4-class)       │
└──────────────┴──────────────────┴──────────────────┘
```
🧪 Feature Framework (225 Features Total)
Category	Count	What It Detects
Header Manipulation	107	IP TTL variance, TCP flag entropy, DNS subdomain entropy, seq. number anomalies
Timing Obfuscation	50	Inter-arrival time patterns, IAT std deviation, timing regularity
Flow Blending	73	Bytes/sec, packet rate variance, flow duration entropy
📋 LOTO Evaluation (Leave-One-Technique-Out)
> The model is tested on steganographic techniques it has **never seen during training** — the most rigorous generalization test.
Split	Technique Withheld	Binary Acc.	Protocol Acc.	FPR
Split 1	Timing Obfuscation	90.60%	92.84%	0.90%
Split 2	Flow Blending	99.05%	91.15%	1.18%
Split 3	Header Manipulation	93.60%	98.93%	0.64%
Mean	—	94.42%	94.30%	0.91%
🗃️ Dataset
13,848 labeled samples — DNS, ICMP, TCP, UDP protocols
Covert tools: dns2tcp, dnscat2, iodine, ptunnel, PingTunnel, Covert TCP, dnsexfiltrator, cobalt strike, OzymanDNS
Behavioral training: All IPs, ports, flow IDs, timestamps stripped — model learns behavior, not infrastructure fingerprints
Lab: Kali Linux Attacker VM + Ubuntu Victim VM (isolated) + NVIDIA Quadro M4000 GPU
🌐 Web Application + Agentic AI Feature
```
┌──────────────────────────────────────────────────────┐
│           Network Steganography Detector              │
│                  Web Application                      │
├──────────────────────────────────────────────────────┤
│  📤 Upload PCAP / CSV network capture                 │
│  ⚡ Real-time Transformer inference (3.8ms/sample)    │
│  📊 Results: Binary · Technique · Protocol output     │
│  🗺️  Attention heatmaps for forensic interpretability │
├──────────────────────────────────────────────────────┤
│  🤖 AGENTIC AI ANALYST                               │
│  • Autonomously interprets detection output           │
│  • Generates SOC-ready incident reports               │
│  • Recommends mitigation strategies per technique     │
│  • Explains attention weights in analyst language     │
└──────────────────────────────────────────────────────┘
```
📁 View Repository →
---
🛡️ SOC Journey
```
[2023] ──► CTF competitions · TryHackMe labs · Network fundamentals & protocols
[2024] ──► SOC Home Lab built · Wazuh SIEM deployed · SSH brute-force simulation & detection
[2024] ──► FYP research begins · Transformer-based Network Steganography detector proposed
[2025] ──► Model trained · 94.42% LOTO accuracy · Outperforms LSTM by 16pp
[2025] ──► Web app + Agentic AI analyst built · Research paper completed
[Now]  ──► Seeking SOC Analyst / Security Researcher roles 🎯
```
Key hands-on labs:
SOC-Lab-BruteForce-SSH — SSH brute force simulation, detected via Wazuh SIEM, incident report written
SOC-Network-Attacks-Lab — Nmap scanning, SMB enumeration, network attack detection
Network-Steganography — FYP: Transformer-based covert channel detector (completed)
Extensive-EDA — Data analysis & visualization pipeline (Spaceship Titanic dataset)
---
🧰 Arsenal
Security & SOC
![Nmap](https://img.shields.io/badge/Nmap-Scanning-4EAA25?style=flat-square&logo=gnu&logoColor=white)
![Wireshark](https://img.shields.io/badge/Wireshark-Forensics-1679A7?style=flat-square&logo=wireshark&logoColor=white)
![Wazuh](https://img.shields.io/badge/Wazuh-SIEM-005571?style=flat-square)
![Metasploit](https://img.shields.io/badge/Metasploit-Exploitation-E34234?style=flat-square)
![Burp Suite](https://img.shields.io/badge/Burp%20Suite-Web%20Testing-FF6633?style=flat-square)
![Scapy](https://img.shields.io/badge/Scapy-Packet%20Crafting-009688?style=flat-square)
AI / ML for Security
![PyTorch](https://img.shields.io/badge/PyTorch-Transformers-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat-square&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Research-F37626?style=flat-square&logo=jupyter&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data-150458?style=flat-square&logo=pandas&logoColor=white)
Languages & Tools
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
---
📊 GitHub Stats
<div align="center">
<img src="https://github-readme-stats.vercel.app/api?username=MalaikaUmbreen&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&include_all_commits=true&bg_color=0D1117&title_color=00D9FF&icon_color=7C3AED" height="165"/>
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=MalaikaUmbreen&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00D9FF" height="165"/>
<br/>
<img src="https://streak-stats.demolab.com?user=MalaikaUmbreen&theme=tokyonight&hide_border=true&background=0D1117&ring=00D9FF&fire=7C3AED&currStreakLabel=00D9FF"/>
<br/>
<img src="https://github-profile-trophy.vercel.app/?username=MalaikaUmbreen&theme=tokyonight&no-frame=true&column=6&margin-w=6&bg_color=0D1117"/>
</div>
---
🤝 Let's Connect
Actively looking for SOC Analyst, Security Researcher, or Junior Penetration Tester roles.
Working on network security, AI-driven threat detection, or covert channel research? Let's connect.
![LinkedIn](https://img.shields.io/badge/LinkedIn-Malaika%20Umbreen-0A66C2?style=for-the-badge&logo=linkedin)
![TryHackMe](https://img.shields.io/badge/TryHackMe-Malaika.Umbreen-212C42?style=for-the-badge&logo=tryhackme&logoColor=red)
---
<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:7C3AED,50:00D9FF,100:0D1117&height=100&section=footer&animation=fadeIn"/>
"Security is not a product, but a process." — Bruce Schneier
</div>
