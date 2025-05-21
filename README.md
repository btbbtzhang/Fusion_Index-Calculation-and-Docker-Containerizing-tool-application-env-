# Fusion_Index Calculation and Docker Containerizing tool application env
To calculated the muscle fiber coverage and fusion index score (nuclear staining inside the fiber percentage) through microscopy images, I found a powerful well-trained Deep Neural Network model that can be used for this purpose, the tool is called MyoFinDer. The objectives of this repository are:   



---

## Aim 1:
To create a proper pipeline workflow for the application of MyoFinDer, so that it can be used for for the lab team daily usage.

## Aim 2:
After smoothly employed this tool, I need to containerize the applying env into a Docker container, so that other biologist can easily use it based on their skills.

Thus, this repository contains two parts.

---

## 📚 Part 1: Tool applicaton, customized workflow and result samples.
(Ref: https://tissueengineeringlab.github.io/MyoFInDer/installation.html#1-on-windows)
Following the documentaion can easily install this tool, it needs to pay extra attention when you are using the IOS operation system or M chips from MAC. This tool uses DNN, which required GPU package from pytorch, however pytorch used Metal Performance Shaders (MPS) for GPU acceleration in M1 chip on MAC, which is far away from the accomplishment at the time when I am using it 2024, it will have some conflicts when you try to use GPU from this tool on M chip MAC computer.  

Back to the topic of workflow, this tool requires iterative looping tuning to rearch to a certain accurency of its calculation. What I meant by iterative looping tuning is that you have to initially start with one parameter set that successfully passed the identifications of most of images for fusion index calculation, then you need multiple parameter sets to go through the failed images iteration by iteration, due to the different image quality or nature of those muscle fibers.  





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
