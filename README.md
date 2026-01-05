<div align="center">

# EdgeVAD: Edge AI for Real-World Video Anomaly Detection

[Kahlil Muchtar (Universitas Syiah Kuala, COMVISLAB USK)](https://comvis.mystrikingly.com/), Al Bahri (Universitas Syiah Kuala), Yudha Nurdin (Universitas Syiah Kuala), [Oky Firmansyah (Nodeflux)](https://www.nodeflux.io/), Alvin Prayuda Juniarta Dwiyantoro (Google), and [Martha Arbayani Zaidan (University of Helsinki)](https://www.marthazaidan.com/) <br>

</div>

<div align="justify">

> **_Abstract:_** _The growing implementation of Intelligent Surveillance Systems (ISS) has heightened the need for Video Anomaly Detection (VAD) to enhance security, reduce labor costs, and improve energy efficiency. Most current VAD methodologies concentrate on delivering superior outcomes based on quantitative metrics, including multimodal techniques, LLM-based models, vision transformers, and sort on. However, these techniques typically demand substantial computational power and are limited to offline operations, rendering them unsuitable for online or real-time VAD surveillance applications. This paper introduces a VAD system based on Edge AI, which integrates a lightweight S3D-based extractor utilizing the Gaussian Error Linear Unit (GeLU) activation function, resulting in an enhanced VAD system. We conduct a comprehensive analysis of the performance of our proposed solution on two well-known edge devices: the Jetson Orin Nano and the ASUS NUC Performance. The analysis encompasses inference speeds, power consumption, and GPU loads across various edge devices. In terms of dataset evaluations, three benchmark datasets (UCF-Crime, XD-Violence, and MSAD) are assessed, demonstrating that our proposed work can attain 86 %, 91%, and 88% of AUC, respectively. These comprehensive insights into the advantages and drawbacks of different edge devices can inform future research and progress in Edge AI technology._

</div>

<div style="position: relative; width: 100%;">
  <img src="media/workflow.jpg" style="width:100%;">
  <div style="
    position: absolute;
    font-style: italic;
    font-size: 14px;
    background: rgba(255,255,255,0.7);
  ">
    Fig. 1. Our proposed EdgeVAD workflow
  </div>
</div>
<br>
<br>

<div align="center">
  <div>
    <div style="display:inline-block; width:45%; vertical-align:middle;">
      <img src="media/jetson.jpg" width="90%">
    </div>
    <div style="display:inline-block; width:45%; vertical-align:middle;">
      <img src="media/asusnoc.jpg" width="90%">
    </div>
  </div>

  <div style="display:flex; justify-content:center; margin-top:4px;">
    <div style="width:45%; text-align:center; font-style:italic; font-size:14px;">
      (a)
    </div>
    <div style="width:45%; text-align:center; font-style:italic; font-size:14px;">
      (b)
    </div>
  </div>

  <div style="margin-top:6px; font-style:italic; font-size:14px; text-align:left;">
    Fig. 2. Physical setting of EdgeVAD in Jetson Orin Nano (a) and ASUS NUC Performance (b).
  </div>
</div>

<br>
<br>

<div align="center" style=" width: 100%; ">
  <img src="media/proposed.jpg" style="width:80%;">
  <div style="
    font-style: italic;
    font-size: 14px;
    background: rgba(255,255,255,0.7);
  ">
    Fig. 3. Proposed Web-Interface Setting of EdgeVAD
  </div>
</div>
<br>

## <img src="https://cdn-icons-png.flaticon.com/512/4149/4149677.png" width="30" style="vertical-align: middle;"/> Data

Please download the data, including S3D-GELU features on UCF-Crime, XD-Violence, MSAD datasets, trained model, and sample videos and corresponding features:

- **S3D-GELU UCF-Crime Features:**  
  [<img src="https://upload.wikimedia.org/wikipedia/commons/d/da/Google_Drive_logo.png" width="18" style="vertical-align: middle;"/> Google Drive Link](https://drive.google.com/drive/folders/1tl_GA9ecUq_Zo8FejsmaXmGGq6a1evMP?usp=sharing)

- **S3D-GELU XD-Violence Features:**  
  [<img src="https://upload.wikimedia.org/wikipedia/commons/d/da/Google_Drive_logo.png" width="18" style="vertical-align: middle;"/> Google Drive Link](https://drive.google.com/drive/folders/13OV2U2SynknxK-RJQX4tqtb81togead_?usp=sharing)

- **S3D-GELU MSAD Features:**  
  [<img src="https://upload.wikimedia.org/wikipedia/commons/d/da/Google_Drive_logo.png" width="18" style="vertical-align: middle;"/> Google Drive Link](https://drive.google.com/drive/folders/1SzMTWWPZ3S9mWE_snSdrw8bsDJyIyZnY?usp=sharing)

## <img src="https://cdn-icons-png.flaticon.com/512/4712/4712109.png" width="30" style="vertical-align: middle;">Trained Models

- **UCF-Crime:**  
  [<img src="https://upload.wikimedia.org/wikipedia/commons/d/da/Google_Drive_logo.png" width="18" style="vertical-align: middle;"/> Google Drive Link](https://drive.google.com/file/d/1nDiF4sjv7V1SzHCkEARAHi-75wMbR0sr/view?usp=sharing)

- **XD-Violence:**  
  [<img src="https://upload.wikimedia.org/wikipedia/commons/d/da/Google_Drive_logo.png" width="18" style="vertical-align: middle;"/> Google Drive Link](https://drive.google.com/file/d/19BvfxD-ZTnZbWWmNkfN4M-SJKHOozhMi/view?usp=sharing)

- **MSAD:**  
  [<img src="https://upload.wikimedia.org/wikipedia/commons/d/da/Google_Drive_logo.png" width="18" style="vertical-align: middle;"/> Google Drive Link](https://drive.google.com/file/d/1WlL6RK8XP7JxhjIiVNM4rG-v1LXvELSr/view?usp=sharing)

- **Link of sample videos and corresponding features:**  
  [<img src="https://upload.wikimedia.org/wikipedia/commons/d/da/Google_Drive_logo.png" width="18" style="vertical-align: middle;"/> Google Drive Link](https://drive.google.com/drive/folders/1O7CT4UHjR1HiAlMuzjhmpYHjQOJu7j4O?usp=sharing)

## Results

- **Results on UCF-Crime**

<p align="center"><b>Table 1. The results of UCF-Crime</b></p>
<div align="center">
    <table >
        <tr style="background-color:#b3b3b3; text-align:center;">
            <th>Supervision</th>
            <th>Method</th>
            <th>Backbone</th>
            <th>AUC</th>
        </tr>
        <tr>
            <td rowspan="10" style="background-color:#b3b3b3; font-weight:bold; text-align:center;">
            Weakly supervised
            </td>
            <td>Sulthani et al. [23]</td>
            <td>C3D RGB</td>
            <td>75.41</td>
        </tr>
        <tr>
            <td>Zhang et al. [53]</td>
            <td>C3D RGB</td>
            <td>78.66</td>
        </tr>
        <tr>
            <td>Motion-Aware [54]</td>
            <td>PWC-Flow</td>
            <td>79.00</td>
        </tr>
        <tr>
            <td>GCN-Anomaly [37]</td>
            <td>TSN-RGB</td>
            <td>82.12</td>
        </tr>
        <tr>
            <td>CLAWS Net [55]</td>
            <td>C3D RGB</td>
            <td>83.03</td>
        </tr>
        <tr>
            <td>CLAWS Net+ [56]</td>
            <td>C3D RGB</td>
            <td>83.37</td>
        </tr>
        <tr>
            <td>CLAWS Net+ [56]</td>
            <td>3DResNext</td>
            <td>84.16</td>
        </tr>
        <tr>
            <td>Wu et al. [16]</td>
            <td>I3D</td>
            <td>82.44</td>
        </tr>
        <tr>
            <td>RTFM [36]</td>
            <td>C3D</td>
            <td>83.28</td>
        </tr>
        <tr>
            <td>RTFM [36]</td>
            <td>I3D</td>
            <td>84.30</td>
        </tr>
        <tr>
            <td rowspan="6" style="background-color:#b3b3b3; font-weight:bold; text-align:center;">
            Lightweight Models
            </td>
            <td>Contrastive [50]</td>
            <td>C3D</td>
            <td>83.40</td>
        </tr>
        <tr>
            <td>Contrastive [50]</td>
            <td>I3D</td>
            <td>84.62</td>
        </tr>
        <tr>
            <td>Watanabe [27]</td>
            <td>I3D</td>
            <td>84.91</td>
        </tr>
        <tr>
            <td>BE-WSVAD [57]</td>
            <td>I3D</td>
            <td>84.1</td>
        </tr>
        <tr>
            <td>Wang et al. [28]</td>
            <td>I3D</td>
            <td>84.7</td>
        </tr>
        <tr>
            <td>STVAD [5]</td>
            <td>I3D</td>
            <td>84.98</td>
        </tr>
        <tr style="font-weight:bold;">
            <td></td>
            <td>Ours</td>
            <td>S3D</td>
            <td style="color:red;">86.0</td>
        </tr>
    </table>
</div>

- **Results on UCF-Crime**

<p align="center"><b>Table 1. The results of UCF-Crime</b></p>
<div align="center">
    <table >
        <tr style="background-color:#b3b3b3; text-align:center;">
            <th>Supervision</th>
            <th>Method</th>
            <th>Backbone</th>
            <th>AUC</th>
        </tr>
        <tr>
            <td rowspan="10" style="background-color:#b3b3b3; font-weight:bold; text-align:center;">
            Weakly supervised
            </td>
            <td>Sulthani et al. [23]</td>
            <td>C3D RGB</td>
            <td>75.41</td>
        </tr>
        <tr>
            <td>Zhang et al. [53]</td>
            <td>C3D RGB</td>
            <td>78.66</td>
        </tr>
        <tr>
            <td>Motion-Aware [54]</td>
            <td>PWC-Flow</td>
            <td>79.00</td>
        </tr>
        <tr>
            <td>GCN-Anomaly [37]</td>
            <td>TSN-RGB</td>
            <td>82.12</td>
        </tr>
        <tr>
            <td>CLAWS Net [55]</td>
            <td>C3D RGB</td>
            <td>83.03</td>
        </tr>
        <tr>
            <td>CLAWS Net+ [56]</td>
            <td>C3D RGB</td>
            <td>83.37</td>
        </tr>
        <tr>
            <td>CLAWS Net+ [56]</td>
            <td>3DResNext</td>
            <td>84.16</td>
        </tr>
        <tr>
            <td>Wu et al. [16]</td>
            <td>I3D</td>
            <td>82.44</td>
        </tr>
        <tr>
            <td>RTFM [36]</td>
            <td>C3D</td>
            <td>83.28</td>
        </tr>
        <tr>
            <td>RTFM [36]</td>
            <td>I3D</td>
            <td>84.30</td>
        </tr>
        <tr>
            <td rowspan="6" style="background-color:#b3b3b3; font-weight:bold; text-align:center;">
            Lightweight Models
            </td>
            <td>Contrastive [50]</td>
            <td>C3D</td>
            <td>83.40</td>
        </tr>
        <tr>
            <td>Contrastive [50]</td>
            <td>I3D</td>
            <td>84.62</td>
        </tr>
        <tr>
            <td>Watanabe [27]</td>
            <td>I3D</td>
            <td>84.91</td>
        </tr>
        <tr>
            <td>BE-WSVAD [57]</td>
            <td>I3D</td>
            <td>84.1</td>
        </tr>
        <tr>
            <td>Wang et al. [28]</td>
            <td>I3D</td>
            <td>84.7</td>
        </tr>
        <tr>
            <td>STVAD [5]</td>
            <td>I3D</td>
            <td>84.98</td>
        </tr>
        <tr style="font-weight:bold;">
            <td style="background-color:#b3b3b3;"></td>
            <td>Ours</td>
            <td>S3D</td>
            <td style="color:red;">86.0</td>
        </tr>
    </table>
</div>

## Qualitative Results

## Citation

Please consider citing our paper in your publications if the project helps your research.

```
“EdgeVAD: Edge AI for Real-World Video Anomaly Detection”, submitted to OJSP, 2026.
```

<br>
<br>

<div align="center" style="position: relative; width: 100%;">
  <img src="media/qualitative.jpg" style="width:70%;">
  <img src="media/qualitative2.jpg" style="width:70%;">
  <img src="media/qualitative3.jpg" style="width:70%;">
  <div style="
    position: absolute;
    font-style: italic;
    font-size: 14px;
    background: rgba(255,255,255,0.7);
  ">
    Fig. 4. Qualitative analysis of tested videos. The red dotted box shows ground truth values, the green curve indicates the anomaly score, the red box frames show anomaly events, and the yellow box frames indicate normal events. (a) Fighting033, (b) Normal006, (c) Young.And.Dangerous.I.1996 (B6 – Car Accident), (d) Before.Sunrise (Normal), (e) Water Incident – 4, and (f) Normal Testing -7.
  </div>
</div>
