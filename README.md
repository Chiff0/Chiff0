<!-- ─────────────────────────────  HEADER  ───────────────────────────── -->
<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&height=200&color=0:0d1117,50:76b900,100:0d1117&text=Filip%20Dobnikar&fontColor=ffffff&fontSize=52&fontAlignY=38&desc=bare-metal%20%E2%80%A2%20GPUs%20%E2%80%A2%20computer%20vision&descAlignY=60&descSize=18" width="100%"/>

<a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&pause=1000&color=76B900&center=true&vCenter=true&width=620&lines=Writing+CUDA+%26+PTX+kernels+by+hand;Squeezing+accuracy-per-watt+out+of+a+Jetson;No+frameworks.+Just+registers.;Embedded+%C3%97+Edge+AI+%C3%97+Vision" alt="Typing SVG" /></a>

<br/>

<img src="https://img.shields.io/badge/📍_Ljubljana,_Slovenia-0d1117?style=for-the-badge"/>
<img src="https://img.shields.io/badge/🎓_FRI_·_University_of_Ljubljana-0d1117?style=for-the-badge"/>
<img src="https://img.shields.io/badge/🇳🇱_Next:_MSc_@_TU_Delft-0d1117?style=for-the-badge"/>

</div>

---

## `$ whoami`

```cpp
struct Filip {
    const char* role      = "Final-year CS student @ FRI, Univ. of Ljubljana";
    const char* lab       = "ViCoS — Visual Cognitive Systems Lab";
    const char* next      = "MSc Computer & Embedded Systems Eng. @ TU Delft";
    const char* thesis    = "Hand-written C++/CUDA/PTX inference engine";
    const char* langs[2]  = {"Slovenian (native)", "English (C2)"};

    // what keeps me up at night
    const char* interests[4] = {
        "GPU kernels & low-level performance",
        "edge AI on power-constrained hardware",
        "embedded systems & robotics",
        "brain–machine interfaces & neural prosthetics",
    };
};
```

---

## 🔥 Currently building

<table>
<tr>
<td width="60%" valign="top">

### ⚡ A from-scratch inference engine for the Jetson Orin Nano

My bachelor's thesis: a YOLO inference engine written in **C++, CUDA and hand-tuned PTX** — no PyTorch, no TensorRT, no ONNX. Just custom kernels, a Darknet `.cfg`/`.weights` parser, and a power meter.

It's benchmarked head-to-head against **Darknet, TensorRT and ONNX Runtime**, and the score that matters is **accuracy-per-watt**, measured live off the board's **INA3221** power monitor.

</td>
<td width="40%" valign="top">

```text
 progress
 ─────────────────────────────
 ✅ Darknet cfg/weights parser
 ✅ CPU FP32 forward pass
 ✅ YOLO layer · decode · NMS
 ✅ validated vs Darknet outputs
 🔄 CUDA / PTX port
 ⏳ INT8 quantization
 ⏳ power-aware benchmarking
```

</td>
</tr>
</table>

```mermaid
flowchart LR
    A[".cfg + .weights"] --> B["Parser"]
    B --> C["Layer graph"]
    C --> D["CUDA / PTX kernels"]
    D --> E["YOLO decode + NMS"]
    E --> F["🎯 detections"]
    D -. "INA3221" .-> G["⚡ watts"]
    F --> H{{"accuracy / watt"}}
    G --> H
```

---

## 🧰 Toolbox

<div align="center">

**Systems & GPU**<br/>
<img src="https://skillicons.dev/icons?i=cpp,c,rust,go&theme=dark"/>
<img src="https://img.shields.io/badge/CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=white" height="48"/>
<img src="https://img.shields.io/badge/PTX-1a1a1a?style=for-the-badge&logo=nvidia&logoColor=76B900" height="48"/>

**Embedded & Robotics**<br/>
<img src="https://img.shields.io/badge/STM32-03234B?style=for-the-badge&logo=stmicroelectronics&logoColor=white"/>
<img src="https://img.shields.io/badge/Jetson_Orin_Nano-76B900?style=for-the-badge&logo=nvidia&logoColor=white"/>
<img src="https://img.shields.io/badge/ROS_2-22314E?style=for-the-badge&logo=ros&logoColor=white"/>
<img src="https://img.shields.io/badge/TurtleBot-1a1a1a?style=for-the-badge&logo=ros&logoColor=white"/>

**Vision & ML**<br/>
<img src="https://skillicons.dev/icons?i=python,opencv&theme=dark"/>
<img src="https://img.shields.io/badge/YOLO-00FFFF?style=for-the-badge&logo=yolo&logoColor=black" height="48"/>
<img src="https://img.shields.io/badge/Darknet-000000?style=for-the-badge&logoColor=white" height="48"/>

**Backend**<br/>
<img src="https://skillicons.dev/icons?i=java,quarkus,docker,postgres,linux,git&theme=dark"/>

</div>

---

## 🛠️ Things I've built

| Project | What it is | Stack |
|---|---|---|
| 🍩 **[STM-Donut-Clicker](https://github.com/Chiff0/STM-Donut-Clicker)** | The classic ASCII spinning donut — reborn as a clicker game on an STM32 board | `C` `STM32` |
| 🤖 **RINS Robotics** | Autonomous TurtleBot: navigation, ring detection & perception with ROS 2 | `ROS 2` `Python` `OpenCV` |
| 👁️ **Anomaly detection** | Computer-vision work on detecting defects and anomalies | `Python` `YOLO` |
| ⚡ **Inference engine** *(thesis)* | Framework-free YOLO inference, optimized for accuracy-per-watt | `C++` `CUDA` `PTX` |

<details>
<summary><b>🍩 psst — click for a donut</b></summary>

```text
                   $$$$$$$$$$$$$@$$
               ####*#############$$$$$$
              *!!!!!!!*!!!*********#######
            ==!==!===!!!!!!!!!!*!!********##
            ;;=;;;::;;;;;;;;;;====!!!!!*!*****
           :;::~~~--------~~~::::;;;===!=!!!!!!
            ~--,,.........,,----~~~:::;;;===!!=
            ,...................,,--~~:::;;;;;=;
            ............:= .........,--~~~::::;;
             ..........,=*#$@$#........,---~~~::
               ......,~:=*#$$#!;,........,,----
                 ...,-~;=*!!!==:-..........,,,
                    ..-~;==!!;;:-,...........
                         .,,----,,........
```

*Rendered with the same math that spins on the STM32.*

</details>

---

## 💼 Experience

```diff
+ Backend Developer (student)  ·  Sunesis d.o.o.                      Oct 2025 – Mar 2026
  Java / Quarkus services

+ Backend Developer (student)  ·  FRI — Lab for Integration of        May 2025 – Sep 2025
                                   Information Systems
```

---

## 🧭 Where I'm headed

> Right now I'm going deep on **CUDA, modern C++, concurrency and hardware-aware software** — and contributing back to the tools I use, starting with **Darknet**.
>
> Long-term, I want to work on technology that genuinely changes things for people. The one I can't stop thinking about: **brain–machine interfaces and neural prosthetics** — where real-time, low-power compute meets the brain.

---

## 📊 Stats

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=Chiff0&show_icons=true&theme=github_dark&hide_border=true&include_all_commits=true&count_private=true&title_color=76b900&icon_color=76b900"/>
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Chiff0&layout=compact&theme=github_dark&hide_border=true&langs_count=8&title_color=76b900"/>

<img width="98%" src="https://github-readme-activity-graph.vercel.app/graph?username=Chiff0&bg_color=0d1117&color=76b900&line=76b900&point=ffffff&area=true&hide_border=true"/>

</div>

---

<div align="center">

<sub>⚙️ <code>nvcc -O3 -arch=sm_87 life.cu -o filip</code> ⚙️</sub>

<img src="https://capsule-render.vercel.app/api?type=waving&height=100&color=0:0d1117,50:76b900,100:0d1117&section=footer" width="100%"/>

</div>
