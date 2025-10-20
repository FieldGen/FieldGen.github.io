# FieldGen: From Teleoperated Pre-Manipulation Trajectories to Field-Guided Data Generation

Official project page for the paper "FieldGen: From Teleoperated Pre-Manipulation Trajectories to Field-Guided Data Generation"

**Status**: Under Review (2025)

## 👥 Authors

**Wenhao Wang**<sup>*2</sup>, **Kehe Ye**<sup>*2,4</sup>, **Xinyu Zhou**<sup>*2,5</sup>, **Tianxing Chen**<sup>*3,4</sup>, Cao Min<sup>5</sup>, Qiaoming Zhu<sup>5</sup>, Xiaokang Yang<sup>1</sup>, Yongjian Shen<sup>2</sup>, Yang Yang<sup>2,†</sup>, Maoqing Yao<sup>2</sup>, Yao Mu<sup>†1</sup>

<sup>*</sup>Equal Contribution  
<sup>†</sup>Corresponding Author

### Affiliations
- <sup>1</sup>MoE Key Lab of Artificial Intelligence, AI Institute, SJTU
- <sup>2</sup>AgiBot
- <sup>3</sup>HKU MMLab
- <sup>4</sup>Lumina Group
- <sup>5</sup>School of Computer Science and Technology, Soochow University

## 🌐 Live Website

Visit: https://fieldgen.github.io

## 📋 Overview

FieldGen is a field-guided framework for scalable robotic manipulation data collection with minimal human involvement. This website showcases:

- **Demo Video**: Interactive demonstration of FieldGen's capabilities
- **Pre-Manipulation Field (PMF)**: Novel field-based approach combining cone fields (position) and spherical fields (orientation)
- **Phase-Decoupled Collection**: Separating pre-manipulation reach and fine manipulation phases
- **Comprehensive Results**: 
  - Equal-time data effectiveness across 4 manipulation tasks
  - Generalization performance (start poses, object positions, unseen objects)
  - Trajectory diversity and spatial coverage analysis
- **Ablation Studies**: Curve types, step sizes (β parameter)
- **Data Collection Efficiency**: Collection rate and capture ratio analysis

## 🏗️ Repository Structure

```
FieldGen.github.io/
├── index.html              # Main webpage
├── README.md              # This file
├── static/
│   ├── css/
│   │   ├── bulma.min.css           # Bulma CSS framework
│   │   ├── bulma-carousel.min.css  # Carousel component
│   │   ├── bulma-slider.min.css    # Slider component
│   │   ├── fontawesome.all.min.css # Icon library
│   │   └── index.css               # Custom styles (gradients, animations)
│   ├── js/
│   │   ├── bulma-carousel.min.js   # Interactive carousel
│   │   ├── bulma-slider.min.js     # Interactive sliders
│   │   ├── fontawesome.all.min.js  # Icon support
│   │   └── index.js                # Custom interactions & scroll effects
│   ├── images/
│   │   ├── teaser.jpg              # Main teaser figure
│   │   ├── pipeline.jpg            # Method overview
│   │   ├── cone_field.png          # Cone field visualization (converted from PDF)
│   │   ├── spherical_field.png     # Spherical field visualization (converted from PDF)
│   │   ├── setup_Pick.jpg          # Pick task setup
│   │   ├── setup_RotatePick.jpg    # Rotate Pick task setup
│   │   ├── setup_TransparentPick.jpg  # Transparent Pick task setup
│   │   ├── setup_AffordancePick.jpg   # Affordance Pick task setup
│   │   ├── setup_exp2.jpg          # Generalization experiment setup
│   │   ├── mainexp1_12panel.png    # Equal-time effectiveness results
│   │   ├── mainexp2_12panel.png    # Generalization results
│   │   ├── diversity_plot.png      # Trajectory diversity analysis
│   │   ├── abla_curve.png          # Curve type ablation
│   │   ├── abla_beta.png           # Step size (β) ablation
│   │   ├── capture_ratio.png       # Capture ratio analysis
│   │   └── rate_window_ema.png     # Collection rate analysis
│   ├── pdfs/
│   │   ├── FieldGen.pdf            # Main paper
│   │   ├── cone_field.pdf          # Original cone field figure (PDF)
│   │   ├── spherical_field.pdf     # Original spherical field figure (PDF)
│   │   └── ...
│   └── videos/
│       ├── Demo_FieldGen.mp4       # Main demonstration video
│       └── ...
└── CHANGELOG.md           # Detailed change history
```

## 🚀 Local Development

### Quick Start

```bash
# Clone the repository
git clone https://github.com/FieldGen/FieldGen.github.io.git
cd FieldGen.github.io

# Start local server (Python 3)
python3 -m http.server 8000

# Or use Python 2
python -m SimpleHTTPServer 8000

# Open browser to http://localhost:8000
```

### File Conversion Tools

If you need to convert PDF figures to PNG:

```bash
# Install poppler-utils (for pdftoppm)
sudo apt-get install poppler-utils  # Ubuntu/Debian
brew install poppler                 # macOS

# Convert PDF to PNG at 300 DPI
pdftoppm -png -r 300 -singlefile static/pdfs/cone_field.pdf static/images/cone_field
```

## 🎨 Website Features

- **Responsive Design**: Optimized for desktop, tablet, and mobile devices
- **Modern UI**: Built with Bulma CSS framework with custom gradient effects
- **Interactive Elements**: Smooth scrolling, scroll-to-top button, and animated transitions
- **Optimized Layout**: 
  - 2-row grid for task demonstrations (Equal-Time section)
  - Flexbox layouts for consistent image alignment
  - Tight spacing for better visual coherence
- **Accessibility**: Semantic HTML5, ARIA labels, and keyboard navigation support
- **SEO Optimized**: Meta tags, Open Graph, Twitter Cards, and structured data (Schema.org)

## 📝 Citation

```bibtex
@article{FieldGen2025,
  title={FieldGen: From Teleoperated Pre-Manipulation Trajectories to Field-Guided Data Generation},
  author={Wang, Wenhao and Ye, Kehe and Zhou, Xinyu and Chen, Tianxing and Min, Cao and Zhu, Qiaoming and Yang, Xiaokang and Shen, Yongjian and Yang, Yang and Yao, Maoqing and Mu, Yao},
  journal={Under Review},
  year={2025},
  url={https://fieldgen.github.io}
}
```

## 📊 Key Results

- **+41.9% Success Rate**: FieldGen outperforms teleoperation across all time checkpoints (4-20 minutes)
- **90%+ Success**: Achieved in just 20 minutes of data collection time
- **100% Success**: Diffusion Policy reaches perfect performance on 3/4 tasks with FieldGen data
- **18.14% Workspace Coverage**: Significantly higher than teleoperation (9.04% - 15.44%)
- **Robust Generalization**: Superior performance across varied start poses, object positions, and unseen objects

## 🔗 Related Works

- [Diffusion Policy](https://diffusion-policy.cs.columbia.edu/) - RSS 2023
- [RDT: Robot Diffusion Transformer](https://rdt-robotics.github.io/rdt-robotics/) - arXiv 2024
- [ACT: Action Chunking with Transformers](https://tonyzhaozh.github.io/aloha/) - ICRA 2023
- [MimicGen](https://mimicgen.github.io/) - CoRL 2023
- [DemoGen](https://demo-generation.github.io/) - RSS 2025

## � Recent Updates

- **2025-01-20**: Added Soochow University affiliation, updated author information with corresponding author
- **2025-01-20**: Added generalization experiment setup image (setup_exp2.jpg)
- **2025-01-20**: Optimized layout spacing and image alignment across all sections
- **2025-01-20**: Converted Field Construction figures from PDF to PNG (300 DPI)
- **2025-01-20**: Reorganized page structure (Demo Video moved before Abstract, Teaser embedded in Abstract)
- **2025-01-20**: Added gradient effect to "FieldGen" title (blue to orange)
- **2025-01-20**: Improved Equal-Time section with 2x2 task image grid

See [CHANGELOG.md](CHANGELOG.md) for detailed update history.

## �📄 Website License

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).

Template adapted from [Academic Project Page Template](https://github.com/eliahuhorwitz/Academic-project-page-template).

---

**Contact**: For questions about this work, please contact Yang Yang (Corresponding Author) at AgiBot.
