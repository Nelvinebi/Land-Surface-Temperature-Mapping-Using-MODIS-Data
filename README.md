# Land Surface Temperature Mapping Using MODIS Data (Synthetic)

This project simulates the use of MODIS satellite data to calculate Land Surface Temperature (LST) using a simplified split-window algorithm. It generates synthetic thermal band data, NDVI, and emissivity to map surface temperatures across a grid of spatial coordinates.

---

## 📌 Project Overview

Land Surface Temperature (LST) is a critical environmental indicator used in climate studies, urban heat assessment, and land monitoring. This project creates a synthetic dataset to demonstrate how MODIS bands (Band 31 & 32) and NDVI can be combined to compute LST using remote sensing methods.

---

## 🧪 Features Simulated

- **T31_K** – Brightness temperature from MODIS Band 31 (Kelvin)
- **T32_K** – Brightness temperature from Band 32 (Kelvin)
- **NDVI** – Normalized Difference Vegetation Index
- **Emissivity** – Estimated from NDVI
- **LST_K** – Calculated Land Surface Temperature in Kelvin
- **LST_Celsius** – Land Surface Temperature in Celsius
- **x_coord / y_coord** – Synthetic spatial positions

---

## 🛠 Technologies Used

- Python 3
- NumPy, pandas
- Matplotlib, Seaborn

---

## 📂 Repository Structure

📁 lst-mapping-modis
├── land_surface_temperature_data.xlsx # Synthetic dataset (200 points)
├── lst_mapping.py # Python script for calculation & visualization
├── README.md # Project overview and usage

yaml
Copy
Edit

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/nelvinebi/lst-mapping-modis.git
   cd lst-mapping-modis
Install required packages:

bash
Copy
Edit
pip install numpy pandas matplotlib seaborn
Run the script:

bash
Copy
Edit
python lst_mapping.py
📈 Output
Computed LST values in Celsius and Kelvin

Visualization of spatial LST distribution using a heatmap

Exported Excel dataset for external analysis or GIS integration

📊 Dataset
The land_surface_temperature_data.xlsx file includes synthetic MODIS-based thermal bands, NDVI, emissivity, and spatial coordinates. It is ideal for demonstrating temperature mapping workflows and geospatial data analysis concepts.

👤 Author

Name: Agbozu Ebingiye Nelvin

Email: nelvinebingiye@gmail.com

GitHub: *github.com/nelvinebi

LinkedIn: *https://www.linkedin.com/in/agbozu-ebi/
