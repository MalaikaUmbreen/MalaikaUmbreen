<div align="center">
<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=30&duration=2800&pause=2000&color=00D9FF&center=true&vCenter=true&width=700&lines=Hi%2C+I'm+Malaika+Umbreen+%F0%9F%91%8B;Cybersecurity+Researcher+%F0%9F%94%90;SOC+Analyst+%7C+AI+for+Network+Defense;Transformer+%2B+Network+Steganography+%F0%9F%A7%A0;Detecting+what+firewalls+cannot+see..." alt="Typing SVG" />
<br/>
`Cybersecurity Researcher · SOC Analyst · AI for Network Defense`
Detecting what firewalls cannot see — covert channels hidden in plain network traffic
<br/>
![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)
![TryHackMe](https://img.shields.io/badge/TryHackMe-Active-red?style=for-the-badge&logo=tryhackme&logoColor=white)
![Profile Views](https://komarev.com/ghpvc/?username=MalaikaUmbreen&style=for-the-badge&color=00d9ff&label=Profile+Views)
<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=80&section=header&animation=twinkling"/>
</div>
---
🔬 Featured Research — FYP ✅ Completed
<div align="center">
A Transformer-based Detector for Network Steganography with Improved Generalization
Air University, Islamabad · Dept. of Cybersecurity · Supervisor: Dr. Zunera Jalil
</div>
> Network steganography hides malicious communication inside normal DNS, ICMP, TCP, and UDP traffic — completely invisible to firewalls and IDS. This research builds a Transformer-based detector that generalises to covert techniques it has never seen before.
📊 Results vs Baselines
Model	Accuracy	AUC-ROC	vs Our Model
🏆 Our Transformer	94.42% ±3.50%	0.981	—
LSTM	78.40% ±6.20%	0.871	−16.02 pp
CNN	76.20% ±5.80%	0.854	−18.22 pp
Random Forest	69.80% ±8.10%	0.802	−24.62 pp
SVM	63.10% ±9.40%	0.743	−31.32 pp
> FPR: **0.91%** · Protocol Attribution: **94.30%** · Technique Classification: **94.52%** · Model Size: **6.9 MB**
> All comparisons significant — McNemar's test, p < 0.001
🏗️ Architecture
```
INPUT → 225 flow-level features (each = 1 attention token, seq. length = 225)
         |
 +-------+-----------------------------------------------+
 |       TRANSFORMER ENCODER (4 blocks)                  |
 |  8-Head Self-Attention  .  FF: 128->256->128 (ReLU)  |
 |  Residual Connections   .  LayerNorm  .  Dropout 0.30 |
 +-------------------------------------------------------+
         | Global Average Pooling
 +---------------+-------------------+--------------------+
 |   HEAD 1      |     HEAD 2        |     HEAD 3         |
 | Binary Detect | Technique Classif | Protocol Attrib    |
 | Normal/Covert | Header / Timing / | DNS/ICMP/TCP/UDP   |
 |  (Sigmoid)    | FlowBlend (4-cls) |   (4-cls softmax)  |
 +---------------+-------------------+--------------------+
```
🧪 Feature Framework — 225 Features Total
Category	Features	Detects
Header Manipulation	107	IP TTL variance, TCP flag entropy, DNS subdomain entropy
Timing Obfuscation	50	Inter-arrival time patterns, IAT std deviation
Flow Blending	73	Bytes/sec, packet rate variance, flow duration entropy
📋 LOTO Evaluation — Tested on Unseen Techniques
Split	Withheld	Binary Acc.	Protocol Acc.	FPR
Split 1	Timing Obfuscation	90.60%	92.84%	0.90%
Split 2	Flow Blending	99.05%	91.15%	1.18%
Split 3	Header Manipulation	93.60%	98.93%	0.64%
Mean	All	94.42%	94.30%	0.91%
🗃️ Dataset — 13,848 Samples
Protocols: DNS · ICMP · TCP · UDP
Covert tools: dns2tcp · dnscat2 · iodine · ptunnel · PingTunnel · Covert TCP · dnsexfiltrator · cobalt strike · OzymanDNS
Behavioral training: All IPs, ports, flow IDs, timestamps stripped — learns behavior, not fingerprints
Lab: Kali Linux Attacker VM + Ubuntu Victim VM + NVIDIA Quadro M4000 GPU
🌐 Web App + Agentic AI Analyst
```
+----------------------------------------------------------+
|            Network Steganography Detector                |
|                   Web Application                        |
+----------------------------------------------------------+
|  Upload PCAP / CSV  .  3.8ms/sample inference            |
|  Binary . Technique . Protocol output                    |
|  Attention heatmaps for forensic interpretability        |
+----------------------------------------------------------+
|  AGENTIC AI ANALYST (built-in)                           |
|  . Autonomously interprets detection results             |
|  . Generates SOC-ready incident reports                  |
|  . Recommends mitigation per technique type              |
|  . Explains attention weights in analyst language        |
+----------------------------------------------------------+
```
View Repository
---
🛡️ SOC Journey
```
[2023] --> CTF competitions . TryHackMe . Network fundamentals & protocols
[2024] --> SOC Home Lab . Wazuh SIEM . SSH brute-force detection
[2024] --> FYP begins . Transformer detector for Network Steganography proposed
[2025] --> 13,848-sample dataset . LOTO 94.42% . Outperforms LSTM by 16pp
[2025] --> Web app + Agentic AI analyst built . Research paper completed
[Now]  --> Open to SOC Analyst / Security Research roles
```
Labs & Projects:
SOC-Lab-BruteForce-SSH — SSH brute force simulation · Wazuh SIEM detection · Incident report
SOC-Network-Attacks-Lab — Nmap · SMB enumeration · Network attack detection
Network-Steganography — FYP: Transformer covert channel detector (completed)
Extensive-EDA — Data analysis & ML pipeline
---
🧰 Tech Stack & Tools
Security & SOC
<p align="left">
<img src="https://img.shields.io/badge/Kali_Linux-557C94?style=for-the-badge&logo=kali-linux&logoColor=white"/>
<img src="https://img.shields.io/badge/Wireshark-1679A7?style=for-the-badge&logo=wireshark&logoColor=white"/>
<img src="https://img.shields.io/badge/Nmap-4EAA25?style=for-the-badge&logo=gnu&logoColor=white"/>
<img src="https://img.shields.io/badge/Metasploit-E34234?style=for-the-badge&logoColor=white"/>
<img src="https://img.shields.io/badge/Burp_Suite-FF6633?style=for-the-badge&logoColor=white"/>
<img src="https://img.shields.io/badge/Wazuh_SIEM-005571?style=for-the-badge&logoColor=white"/>
</p>
AI / ML & Research
<p align="left">
<img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white"/>
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/Scapy-009688?style=for-the-badge&logoColor=white"/>
<img src="https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white"/>
<img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white"/>
<img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white"/>
</p>
Languages & Dev Tools
<p align="left">
<img src="https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white"/>
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"/>
<img src="https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white"/>
<img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white"/>
<img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white"/>
<img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black"/>
<img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white"/>
<img src="https://img.shields.io/badge/VS_Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white"/>
</p>
---
📊 GitHub Stats
<div align="center">
<img width="49%" src="https://github-readme-stats.vercel.app/api?username=MalaikaUmbreen&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&include_all_commits=true"/>
<img width="49%" src="https://github-readme-stats.vercel.app/api/top-langs/?username=MalaikaUmbreen&layout=compact&theme=tokyonight&hide_border=true"/>
<br/>
<img width="70%" src="https://streak-stats.demolab.com?user=MalaikaUmbreen&theme=tokyonight&hide_border=true"/>
<br/>
<img src="https://github-profile-trophy.vercel.app/?username=MalaikaUmbreen&theme=tokyonight&no-frame=true&column=6&margin-w=8"/>
</div>
---
🤝 Let's Connect
> Open to **SOC Analyst · Security Researcher · Junior Penetration Tester** roles.
> Researching network security, AI-driven threat detection, or covert channels? Reach out.
<p align="left">
<a href="https://linkedin.com/in/malaika-umbreen"><img src="https://img.shields.io/badge/LinkedIn-Malaika_Umbreen-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
<a href="https://tryhackme.com/p/Malaika.Umbreen"><img src="https://img.shields.io/badge/TryHackMe-Malaika.Umbreen-212C42?style=for-the-badge&logo=tryhackme&logoColor=red"/></a>
</p>
---
<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=80&section=footer&animation=twinkling"/>
"Security is not a product, but a process." — Bruce Schneier
</div>
