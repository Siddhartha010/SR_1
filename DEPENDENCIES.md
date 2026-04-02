# SRTransGAN - Package Dependencies

## Complete List of Packages and Libraries Used

### 1. **PyTorch Ecosystem**
- **torch** - Core deep learning framework for building and training neural networks
  - Used for: Model architecture, tensor operations, GPU acceleration
  - Files: All .py files
  
- **torchvision** - Computer vision utilities for PyTorch
  - Used for: Image I/O, transforms, data loading
  - Files: utils.py, main.py, test.py
  
- **torch.nn** - Neural network modules
  - Used for: Layers, loss functions, activation functions
  - Files: model.py, SRTransG.py, main.py
  
- **torch.nn.functional** - Functional interface for neural networks
  - Used for: Activation functions (GELU), normalization
  - Files: model.py, SRTransG.py

### 2. **Tensor Operations**
- **einops** - Flexible tensor operations library
  - Used for: Rearranging, repeating tensors in attention mechanisms
  - Functions: rearrange(), repeat()
  - Files: model.py, SRTransG.py

### 3. **Image Processing**
- **Pillow (PIL)** - Python Imaging Library
  - Used for: Image loading, saving, concatenation
  - Files: main.py, test.py, augment.py
  
- **opencv-python (cv2)** - Computer vision library
  - Used for: SSIM calculation, Gaussian filtering
  - Files: utils.py, test.py
  
- **scikit-image (skimage)** - Image processing algorithms
  - Used for: Image I/O, transformations, augmentation
  - Modules: skimage.io, skimage.transform, skimage.util, skimage.filters
  - Files: augment.py

### 4. **Numerical Computing**
- **numpy** - Numerical computing library
  - Used for: Array operations, mathematical computations, PSNR/SSIM calculations
  - Files: utils.py, model.py, test.py, augment.py

### 5. **Visualization**
- **matplotlib** - Plotting and visualization library
  - Used for: Saliency map visualization, color maps
  - Modules: matplotlib.pyplot, matplotlib.cm
  - Files: test.py

### 6. **Utilities**
- **torchsummary** - Model summary and architecture visualization
  - Used for: Displaying model architecture and parameters
  - Files: main.py
  
- **tqdm** - Progress bar library
  - Used for: Training and testing progress visualization
  - Files: main.py, test.py

### 7. **Python Standard Library**
- **os** - Operating system interface
  - Used for: File path operations, directory management
  
- **glob** - File pattern matching
  - Used for: Finding dataset files
  
- **argparse** - Command-line argument parsing
  - Used for: Training/testing configuration
  
- **copy** - Shallow and deep copy operations
  - Used for: Model weight loading
  
- **math** - Mathematical functions
  - Used for: PSNR calculation, grid layout
  
- **logging** - Logging facility
  - Used for: Training logs and experiment tracking
  
- **shutil** - High-level file operations
  - Used for: Directory management
  
- **time** - Time access and conversions
  - Used for: Timestamp logging
  
- **datetime** - Date and time manipulation
  - Used for: Test logging timestamps
  
- **warnings** - Warning control
  - Used for: Suppressing warnings in augment.py
  
- **numbers** - Numeric abstract base classes
  - Used for: Type checking in LayerNorm
  
- **pdb** - Python debugger
  - Used for: Debugging (set_trace)

## Installation

Install all dependencies using:
```bash
pip install -r requirements.txt
```

Or install individually:
```bash
pip install torch torchvision einops Pillow opencv-python scikit-image numpy matplotlib torchsummary tqdm
```

## Version Requirements
- Python: 3.7+
- CUDA: 10.2+ (for GPU support)
- PyTorch: 1.8.0+

## Hardware Requirements
- GPU: NVIDIA GPU with CUDA support (recommended)
- RAM: 16GB+ recommended
- Storage: Sufficient space for datasets and model checkpoints
