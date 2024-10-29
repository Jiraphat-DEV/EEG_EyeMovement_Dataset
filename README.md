## English

# EEG Eye Movement Dataset

This dataset contains EEG (Electroencephalography) data collected during tasks involving eye movements: looking left, normal (looking center), and looking right. The structure of this dataset is organized to be easily accessible for research, particularly in areas related to brain-computer interfaces, machine learning, and deep learning in the context of eye movement analysis.

## Dataset Structure

This dataset is organized as follows:

```
Copy code
EEG_EyeMovement_Dataset
├── Combined_Subjects
│   ├── Combined_X.npy
│   └── Combined_y.npy
├── Individual_Subjects
│   ├── S1
│   │   ├── X_raw_S1.npy
│   │   └── Y_S1.npy
│   ├── S2
│   │   ├── X_raw_S2.npy
│   │   └── Y_S2.npy
│   └── ...
├── Selected_Data
│   ├── Selected_X.npy
│   └── Selected_y.npy
```

### Folder Descriptions:

- **Individual_Subjects**: Contains EEG data processed with a sliding window of 307 samples, consisting of 256 samples for 1 second and 51 preceding samples, for each individual (`S1`, `S2`, ...). Each participant's folder contains `X_raw` for EEG signals and `Y` for labels.
- **Combined_Subjects**: Contains the combined dataset of all participants, where `Combined_X.npy` represents EEG signals and `Combined_y.npy` represents labels.
- **Selected_Data**: Contains data selected from `Combined_Subjects` after a certain level of screening.

## Data Format

- **X_raw_S#.npy**: A Numpy array file containing raw EEG data for each participant.
- **Y_S#.npy**: A Numpy array file containing labels corresponding to the EEG data ("Saccades Left", "Center", "Saccades Right").

## Usage

The dataset can be loaded using the following Python code:

```
python


Copy code
import numpy as np

# Load combined data
X_combined = np.load('Combined_Subjects/Combined_X.npy')
y_combined = np.load('Combined_Subjects/Combined_y.npy')

# Load individual participant data (e.g., Participant 1)
X_S1 = np.load('Individual_Subjects/S1/X_raw_S1.npy')
y_S1 = np.load('Individual_Subjects/S1/Y_S1.npy')
```

## Requirements

- Numpy

To install the required package:

```
Copy code
pip install numpy
```

Dataset Reference

Jiraphat-DEV. (2024). BCIPI. GitHub repository. https://github.com/Jiraphat-DEV/BCIPI





## ภาษาไทย

# EEG Eye Movement Dataset

ชุดข้อมูลนี้ประกอบด้วยข้อมูล EEG (Electroencephalography) ที่เก็บระหว่างการทำงานที่เกี่ยวข้องกับการเคลื่อนไหวดวงตา: มองไปทางซ้าย ปกติ (มองตรงกลาง) และมองไปทางขวา โครงสร้างชุดข้อมูลนี้ถูกจัดเพื่อให้เข้าถึงได้ง่ายสำหรับการวิจัย โดยเฉพาะในด้านที่เกี่ยวข้องกับอินเตอร์เฟซสมองกับคอมพิวเตอร์, การเรียนรู้ของเครื่อง และการเรียนรู้เชิงลึกในบริบทของการวิเคราะห์การเคลื่อนไหวดวงตา

## Dataset Structure

ชุดข้อมูลนี้ถูกจัดตามโครงสร้างดังนี้:

```
EEG_EyeMovement_Dataset
├── Combined_Subjects
│   ├── Combined_X.npy
│   └── Combined_y.npy
├── Individual_Subjects
│   ├── S1
│   │   ├── X_raw_S1.npy
│   │   └── Y_S1.npy
│   ├── S2
│   │   ├── X_raw_S2.npy
│   │   └── Y_S2.npy
│   └── ...
├── Selected_Data
│   ├── Selected_X.npy
│   └── Selected_y.npy
```

### คำอธิบายโฟลเดอร์:

- **Individual_Subjects**: ประกอบด้วยข้อมูล EEG ที่ผ่านการทำ sliding window ขนาด 307sample ประกอบโดย 256 sample ของ 1 วินาที และ 51 sample ก่อนหน้า ของแต่ละบุคคล (`S1`, `S2`, ...). แต่ละโฟลเดอร์ของผู้เข้าร่วมประกอบด้วย `X_raw` สำหรับสัญญาณ EEG และ `Y` สำหรับป้ายกำกับ
- **Combined_Subjects**: ประกอบด้วยชุดข้อมูลรวมของผู้เข้าร่วมทุกคน โดย `Combined_X.npy` แทนสัญญาณ EEG และ `Combined_y.npy` แทนป้ายกำกับ
- **Selected_Data**: ประกอบด้วยชุดข้อมูลที่ถูกคัดเลือกมาจาก `Combined_Subjects` ผ่านการตรวจเช็คระดับหนึ่ง

## รูปแบบข้อมูล

- **X_raw_S#.npy**: ไฟล์ Numpy array ที่ประกอบด้วยข้อมูล EEG ดิบของผู้เข้าร่วมแต่ละราย
- **Y_S#.npy**: ไฟล์ Numpy array ที่ประกอบด้วยป้ายกำกับที่สอดคล้องกับข้อมูล EEG ("Saccades Left", "Center", "Saccades Right")

## การใช้งาน

สามารถโหลดชุดข้อมูลได้โดยใช้โค้ด Python ดังนี้:

```
import numpy as np

# โหลดข้อมูลรวม
X_combined = np.load('Combined_Subjects/Combined_X.npy')
y_combined = np.load('Combined_Subjects/Combined_y.npy')

# โหลดข้อมูลของผู้เข้าร่วมแต่ละราย (เช่น ผู้เข้าร่วม 1)
X_S1 = np.load('Individual_Subjects/S1/X_raw_S1.npy')
y_S1 = np.load('Individual_Subjects/S1/Y_S1.npy')
```

## ความต้องการ

- Numpy

การติดตั้งแพ็กเกจที่ต้องการ:

```
pip install numpy
```

อ้างอิง Dataset

Jiraphat-DEV. (2024). BCIPI. GitHub repository. https://github.com/Jiraphat-DEV/BCIPI