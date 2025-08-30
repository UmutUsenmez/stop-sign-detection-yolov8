## Türkçe Açıklama
Bu proje, YOLOv8 kullanılarak **stop tabelalarının tespiti** için geliştirilmiştir. 
Amaç, trafik işaretlerinin bilgisayarla görü (computer vision) yöntemleriyle 
tanınması ve tespit edilmesidir.

### İçerik
- **dataset/** → Eğitim için kullanılan veri seti (stop tabelası görselleri)
- **outputs/** → Test sonuçlarının görselleri
- **graphs of deep learning algorithm/** → Eğitim sürecinde elde edilen loss/accuracy grafikler
- **Code File.ipynb** → Modelin eğitildiği ve test edildiği notebook dosyası
- **README.md** → Proje açıklaması ve çalıştırma adımları

### Çalıştırma
1. Repoyu klonlayın:
   \`\`\`bash
   git clone https://github.com/UmutUsenmez/stop-sign-detection-yolov8.git
   cd stop-sign-detection-yolov8
   \`\`\`

2. Bağımlılıkları yükleyin:
   \`\`\`bash
   pip install ultralytics
   \`\`\`

3. Eğitilmiş modeli kullanarak test edin:
   \`\`\`python
   from ultralytics import YOLO
   model = YOLO('runs/detect/train/weights/best.pt')
   results = model.predict(source='stop_sign_dataset/test', conf=0.25)
   \`\`\`


## English Description
This project is developed for **stop sign detection** using YOLOv8.  
The goal is to recognize and detect traffic signs with computer vision techniques.

### Contents
- **dataset/** → Dataset used for training (stop sign images)
- **outputs/** → Images of test results
- **graphs of deep learning algorithm/** → Loss/accuracy plots obtained during training
- **Code File.ipynb** → Notebook file for training and testing the model
- **README.md** → Project description and usage instructions

### How to Run
1. Clone the repository:
   \`\`\`bash
   git clone https://github.com/UmutUsenmez/stop-sign-detection-yolov8.git
   cd stop-sign-detection-yolov8
   \`\`\`

2. Install dependencies:
   \`\`\`bash
   pip install ultralytics
   \`\`\`

3. Run inference with the trained model:
   \`\`\`python
   from ultralytics import YOLO
   model = YOLO('runs/detect/train/weights/best.pt')
   results = model.predict(source='stop_sign_dataset/test', conf=0.25)
   \`\`\`

