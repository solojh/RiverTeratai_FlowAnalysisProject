# River Teratai Flow Analysis (Drone Video-Based)
## 🚁 Drone-Based Data Collection

The source video was captured using a **drone-mounted camera** flying over River Teratai. The drone allows for a stable aerial perspective, enabling accurate frame extraction and ground control point (GCP) marking for georectification and flow analysis.

## 📂 Dataset
The dataset for this project is available on Google Drive:
🔗 [River Teratai Data](https://drive.google.com/drive/folders/180sGavZzXUh0TQSTP3UN8WoXxwi1o0_v?usp=sharing)

## 📓 Jupyter Notebook
Since the file is larger than 25MB, the analysis and visualizations are included in this Jupyter Notebook：
🔗 [River Teratai Notebook](https://drive.google.com/file/d/1yk2g2cQFL-JyOuN5u3HAmyAMUFP2ruep/view?usp=sharing)


### **1️⃣ Install Required Packages**  
```bash
pip install pyorc pyopenrivercam cartopy
```  

### **2️⃣ Set Up Camera Configuration**  
- Extract the first frame from `DJI_0724.mp4`.  
- Mark Ground Control Points (GCPs) with corresponding UTM coordinates.  
- Create `CameraConfig` and save as `ngwerere.json`.  

### **3️⃣ Process the Video**  
- Load the `ngwerere.json` camera configuration.  
- Define the stabilized region and process the first 125 frames.  

### **4️⃣ Image Processing**  
- Convert frames to grayscale and normalize contrast.  
- Georectify images and overlay satellite imagery.  

### **5️⃣ Flow Velocity Analysis (Velocimetry)**  
- Compute PIV (Particle Image Velocimetry) and save as `ngwerere_piv.nc`.  
- Load PIV results and visualize velocity fields.  
- Apply masking techniques to refine velocity calculations.  

### **6️⃣ Visualization & Analysis**  
- Display RGB frames with georectified projection.  
- Overlay velocity vector fields with color mapping.  
- Compute time-averaged flow velocity and apply spatial filtering.  

![image](https://github.com/user-attachments/assets/d3bb74c8-5854-4ddc-8a77-df3aec046e0c)





