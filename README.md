# 🎨 Background Removal with rembg

## 📌 Project Description
This project uses the **rembg** library to ✨ remove the background from an image. It processes an uploaded image and saves a transparent background version in PNG format.

## 🔧 Installation & Setup
Run the following command to install the required dependencies:
```bash
!pip install -q rembg pillow numpy onnxruntime
```

After installation, restart the runtime in **Google Colab**:
```python
import os
os._exit(00)  # 🔄 Restart the runtime
```

## 🚀 How to Use
1. **📂 Upload an Image** to Colab.
2. **🖼️ Run the script** to remove the background:
   ```python
   from PIL import Image
   import rembg

   input_path = "/mnt/data/image.png"  # 📝 Update this with the correct path
   output_path = "/mnt/data/image_no_bg.png"

   with Image.open(input_path) as img:
       img_no_bg = rembg.remove(img)
       img_no_bg.save(output_path, format="PNG")

   print(f"✅ Background removed! Saved at: {output_path}")
   ```
3. **⬇️ Download the processed image:**
   ```python
   from google.colab import files
   files.download(output_path)
   ```

## ⚠️ Common Issues & Fixes
- **❌ ModuleNotFoundError: No module named 'rembg'**
  - Restart the runtime after installing rembg.
- **🖼️ OSError: cannot write mode RGBA as JPEG**
  - Save the output as PNG instead of JPEG to support transparency.

## 👤 Author
- 🔗 LinkedIn: [Kartikey](https://www.linkedin.com/in/kartikey05/)

