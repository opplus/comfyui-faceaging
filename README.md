# Face Aging

### Description
- This is a comfyui custom node version of [Age Transformation](https://github.com/yuval-alaluf/SAM)
- You could transform age of target from -100 to +100(but recommended -50 to +100)

### Prerequisites
- Linux or macOS
- NVIDIA GPU + CUDA CuDNN (CPU may be possible with some modifications, but is not inherently supported)
- Python 3

### How to use
1. **clone this repo to `ComfyUI/custom_nodes` folder**
2. **Install PreRequisites**
```bash
sudo apt-get install cmake
pip install dlib, ninja
```
**(Option) If you use in WSL2, should set up CUDA**
```bash
sudo apt install nvidia-cuda-toolkit
```

3. **download models(`sam_ffhq_aging.pt` & `shape_predictor_68_face_landmarks.dat`) to `ComfyUI/models/face_aging`**
```bash
mkdir -p ComfyUI/models/face_aging
pip install gdown
cd models
gdown "https://drive.google.com/u/0/uc?id=1XyumF6_fdAxFmxpFcmPf-q84LU_22EMC&export=download" -O face_aging/sam_ffhq_aging.pt
cd face_aging
wget "https://github.com/italojs/facial-landmarks-recognition/raw/master/shape_predictor_68_face_landmarks.dat"
```
4. **run the comfyUI and use it like this**
![Image](/workflow_example/workflow.png)
