# 🌍 GEE Workshop: การวิเคราะห์ข้อมูลอุตุ-อุทก-ไฟป่า-คุณภาพน้ำ ด้วย Google Earth Engine

**Meteorology · Hydrology · Wildfire · Water Quality Analysis with GEE Python API**

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](#-notebooks)
[![GEE](https://img.shields.io/badge/Google%20Earth%20Engine-4285F4?logo=google-earth&logoColor=white)](#)
[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?logo=python&logoColor=white)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](#license)

---

## 📖 เกี่ยวกับ Workshop นี้

Workshop สอนการใช้ **Google Earth Engine (GEE) Python API** ร่วมกับ **Google Colab** เพื่อวิเคราะห์ข้อมูลด้านสิ่งแวดล้อม 4 หัวข้อ โดยใช้พื้นที่ประเทศไทยเป็นกรณีศึกษา เหมาะสำหรับนักศึกษา นักวิจัย และผู้ที่สนใจด้าน Remote Sensing และ Geospatial Data Science

**ระยะเวลา:** 3 ชั่วโมง (9:00 - 12:00)

---

## 📅 ตารางเวลา

| ช่วง | เวลา | Module | เนื้อหา |
|------|-------|--------|---------|
| **ช่วงที่ 1** | 9:00 - 9:45 | Module 1: อุตุนิยมวิทยา | ปริมาณฝน, อุณหภูมิ, Rainfall Anomaly |
| | 9:45 - 10:30 | Module 2: อุทกวิทยา | พื้นผิวน้ำ, น้ำท่วม SAR, ความชื้นดิน |
| ☕ **พักเบรค** | 10:30 - 10:45 | | |
| **ช่วงที่ 2** | 10:45 - 11:20 | Module 3: ไฟป่า | จุดความร้อน, พื้นที่เผาไหม้, dNBR |
| | 11:20 - 11:55 | Module 4: คุณภาพน้ำ | ความขุ่น, คลอโรฟิลล์, ตะกอน, SST |
| **สรุป** | 11:55 - 12:00 | | Q&A |

---

## 📓 Notebooks

| # | ไฟล์ | หัวข้อ | Open in Colab |
|---|------|--------|---------------|
| 1 | [`01_Meteorology_GEE.ipynb`](01_Meteorology_GEE.ipynb) | 🌦️ อุตุนิยมวิทยา (Meteorology) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/SitthisakMoukomla/gee-forest-meteorology/blob/main/01_Meteorology_GEE.ipynb) |
| 2 | [`02_Hydrology_GEE.ipynb`](02_Hydrology_GEE.ipynb) | 💧 อุทกวิทยา (Hydrology) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/SitthisakMoukomla/gee-forest-meteorology/blob/main/02_Hydrology_GEE.ipynb) |
| 3 | [`03_Wildfire_GEE.ipynb`](03_Wildfire_GEE.ipynb) | 🔥 ไฟป่า (Wildfire) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/SitthisakMoukomla/gee-forest-meteorology/blob/main/03_Wildfire_GEE.ipynb) |
| 4 | [`04_WaterQuality_GEE.ipynb`](04_WaterQuality_GEE.ipynb) | 🌊 คุณภาพน้ำ (Water Quality) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/SitthisakMoukomla/gee-forest-meteorology/blob/main/04_WaterQuality_GEE.ipynb) |

> 💡 Colab badge จะเปิด Notebook โดยตรงจาก GitHub repo `SitthisakMoukomla/gee-forest-meteorology`

---

## 🗂️ Datasets ที่ใช้

### Module 1: อุตุนิยมวิทยา
| Dataset | รายละเอียด | Resolution | GEE ID |
|---------|-----------|------------|--------|
| CHIRPS Daily | ปริมาณฝนรายวัน (1981-ปัจจุบัน) | ~5.5 km | `UCSB-CHG/CHIRPS/DAILY` |
| ERA5-Land Monthly | อุณหภูมิ, ลม, ฯลฯ (1950-ปัจจุบัน) | ~11 km | `ECMWF/ERA5_LAND/MONTHLY_AGGR` |

### Module 2: อุทกวิทยา
| Dataset | รายละเอียด | Resolution | GEE ID |
|---------|-----------|------------|--------|
| JRC Global Surface Water | แผนที่น้ำผิวดิน (1984-2021) | 30 m | `JRC/GSW1_4/GlobalSurfaceWater` |
| JRC Monthly History | พื้นที่น้ำรายเดือน | 30 m | `JRC/GSW1_4/MonthlyHistory` |
| Sentinel-1 SAR GRD | ภาพเรดาร์ (ตรวจน้ำท่วม) | 10 m | `COPERNICUS/S1_GRD` |
| Sentinel-2 SR | ภาพถ่ายดาวเทียม (NDWI) | 10 m | `COPERNICUS/S2_SR_HARMONIZED` |

### Module 3: ไฟป่า
| Dataset | รายละเอียด | Resolution | GEE ID |
|---------|-----------|------------|--------|
| MODIS Active Fire | จุดความร้อนรายวัน | 1 km | `MODIS/061/MOD14A1` |
| FIRMS | จุดความร้อน VIIRS | 1 km | `FIRMS` |
| MODIS Burned Area | พื้นที่เผาไหม้รายเดือน | 500 m | `MODIS/061/MCD64A1` |
| Sentinel-5P | Aerosol Index (มลพิษอากาศ) | ~5.5 km | `COPERNICUS/S5P/OFFL/L3_AER_AI` |

### Module 4: คุณภาพน้ำ
| Dataset | รายละเอียด | Resolution | GEE ID |
|---------|-----------|------------|--------|
| Sentinel-2 SR | ดัชนีคุณภาพน้ำ (NDTI, NDCI, TSS) | 10 m | `COPERNICUS/S2_SR_HARMONIZED` |
| NOAA OISST | Sea Surface Temperature (รายวัน, 1981-ปัจจุบัน) | ~27 km | `NOAA/CDR/OISST/V2_1` |

---

## 🔧 สิ่งที่ต้องเตรียมก่อนเริ่ม

### 1. สมัคร Google Earth Engine
- ไปที่ [earthengine.google.com](https://earthengine.google.com/) แล้วสมัครด้วย Google Account
- สร้าง **Cloud Project** ที่ [console.cloud.google.com](https://console.cloud.google.com/)
- เปิดใช้งาน **Earth Engine API** ใน Cloud Console

### 2. เตรียม Google Colab
- เปิด [colab.research.google.com](https://colab.research.google.com/)
- Login ด้วย Google Account เดียวกับที่สมัคร GEE

### 3. แก้ไข Project ID
ในทุก Notebook ให้เปลี่ยนบรรทัดนี้:
```python
ee.Initialize(project='YOUR-PROJECT-ID')
```
เป็น Cloud Project ID ของคุณ เช่น:
```python
ee.Initialize(project='my-gee-project-12345')
```

---

## 📐 ดัชนีที่ใช้ในการวิเคราะห์

| ดัชนี | สูตร | การใช้งาน |
|-------|------|----------|
| **NDWI** | (Green − NIR) / (Green + NIR) | ตรวจจับพื้นที่น้ำ |
| **MNDWI** | (Green − SWIR) / (Green + SWIR) | ตรวจจับน้ำในพื้นที่เมือง |
| **NBR** | (NIR − SWIR2) / (NIR + SWIR2) | วัดความรุนแรงของไฟ |
| **dNBR** | NBR_before − NBR_after | จำแนกระดับความเสียหายจากไฟ |
| **NDTI** | (Red − Green) / (Red + Green) | ความขุ่นของน้ำ |
| **NDCI** | (RedEdge − Red) / (RedEdge + Red) | คลอโรฟิลล์-เอในน้ำ |

---

## 🌏 พื้นที่ศึกษา

| Module | พื้นที่หลัก | จังหวัด/บริเวณ |
|--------|-----------|----------------|
| อุตุนิยมวิทยา | ทั่วประเทศไทย | เชียงใหม่, กรุงเทพฯ, นครราชสีมา, สุราษฎร์ธานี, อุดรธานี |
| อุทกวิทยา | ภาคกลาง | กรุงเทพฯ, นนทบุรี, ปทุมธานี, อยุธยา |
| ไฟป่า | ภาคเหนือ | เชียงใหม่, เชียงราย, แม่ฮ่องสอน, ลำปาง, น่าน, แพร่ |
| คุณภาพน้ำ | ชายฝั่ง + อ่างเก็บน้ำ | อ่าวไทยตอนบน, ทะเลสาบสงขลา, เขื่อนภูมิพล |

---

## 📦 Libraries ที่ใช้

```
earthengine-api
geemap
pandas
matplotlib
numpy
```

ใน Google Colab ส่วนใหญ่มีติดตั้งอยู่แล้ว ยกเว้น `geemap`:
```bash
pip install geemap --quiet
```

---

## 📚 แหล่งเรียนรู้เพิ่มเติม

- [GEE Python API Documentation](https://developers.google.com/earth-engine/guides/python_install)
- [GEE Dataset Catalog](https://developers.google.com/earth-engine/datasets)
- [geemap Documentation](https://geemap.org/)
- [Awesome GEE Community Datasets](https://gee-community-catalog.org/)
- [GEE Q&A on GIS StackExchange](https://gis.stackexchange.com/questions/tagged/google-earth-engine)

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Google Earth Engine Team
- [geemap](https://geemap.org/) by Dr. Qiongqiong Wu
- CHIRPS, ERA5, Sentinel, MODIS data providers
