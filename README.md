# Fusion_Index Calculation and Docker Containerizing tool application env
Our biotech company, Myo Palate aims to grow cultivative meat from the lab, thus all muscle related bio calculations require some explorations. To assess myo cellular fusing status, we used fluorescent staining method to dye muscle cells and DNA (nuclei), then tool MyoFinDer can be employed to effienctly detect and draw out the muscle fiber coverage (nuclear staining inside the fiber percentage) through microscopy images, as well as the calculation of fusion index score. Going through the iteratures, I found this powerful Deep Neural Network model that has been already well trained on many biological images databases. So from the aspect of computation views, the objectives of this repository are:   



---

## Aim 1:
To create a proper pipeline and workflow for the practical application of MyoFinDer, so that it can be used for for the lab team daily usage.

## Aim 2:
After smoothly employed this tool, I need to containerize the applying env into a Docker container, so that other biologist or nonexpert can easily, simply use it based on their skills.

Thus, this repository contains two parts.

---

## 📚 Part 1: Tool applicaton, customized workflow and result samples.
(Ref: https://tissueengineeringlab.github.io/MyoFInDer/installation.html#1-on-windows)
Following the documentaion can easily install this tool, just needs to pay extra attentions when you are using the IOS operation system or M chips from MAC. This tool uses DNN, which required GPU package from pytorch, however pytorch used Metal Performance Shaders (MPS) for GPU acceleration in M1 chip on MAC, which is far away from the accomplishment at the time when I am using it in early 2024, it will have some conflicts when you try to use GPU from this tool on M chip MAC computer.  

  Back to the topic of workflow, this tool requires iterative tuning strategy to rearch to a certain accurency of its calculation. What I meant by iterative tuning is that you have to initially start with one parameter set that successfully passed the identifications of most of images for fusion index calculation, then you need to use different multiple parameter sets to go through all failed images by next iterations, due to the different image quality or nature of those muscle fibers. 

### GUI for MyoFinDer
![Screenshot 2024-10-24 115252](https://github.com/user-attachments/assets/c9ef921c-300f-4c3d-9629-e2b97eacddca)

From right window of the above figure, select the correct options that associated with your image proporties, we could use the defaulted setting to initiate fusion index calculations. The following figures showed some examples of how fiber and nuclei detection by MyoFinDer.
![Screenshot 2024-10-28 153542](https://github.com/user-attachments/assets/74543f00-54a5-489e-850b-d2a3ddd284ec)
Where, the highlighted red regions are the identified muscle fibers, and the red dots are the nuclei detected not inside the fibers, while the yellow ones are the ones inside them.<br>
The final output will contain two subfolders that have original and processed detected figures. Two pickle format data for file recovery or records, and the final numeric execel sheet for all calculation results.
![Screenshot 2025-05-26 121936](https://github.com/user-attachments/assets/58cc4eb5-8297-4167-93ce-ed98fcceb7f2)

Notably, tool MyoFinDer does not heavily rely on the quality of input images, the numeric calculation is kinda strongly associating with the image detection results, which the values vary significantly if the image results changed. This factor also decides that we need to do further in our iterative tuning process to have reliable results.


### Customized Workflow

![Screenshot 2025-05-22 093709](https://github.com/user-attachments/assets/f78f3d91-0d2e-4571-b0a2-f36cf805b85f)


![Screenshot 2025-05-22 100521](https://github.com/user-attachments/assets/38c87168-d6e0-4bd0-9b27-e8f68a611aff)




---

## ✨ **Design Tips and Styles**

### ✅ Use Emojis for Visual Cue

- 📝 For "Getting Started"
- 📦 For "Installation"
- ⚙️ For "Configuration"
- 💡 For "Usage"
- 🔧 For "Development"
- 📄 For "API Reference"
- 🛠 For "Contributing"
- 🐛 For "Issues"
- 📜 For "License"

This enhances readability and makes it more inviting.

---

### ✅ Use Shields.io Badges

Add dynamic status badges:

```markdown
![License](https://img.shields.io/badge/license-MIT-blue.svg)
