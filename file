import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# 1. Generate Synthetic MODIS-like Data
np.random.seed(42)
n_points = 200  # >150 points

# Coordinates (for mapping)
x_coords = np.random.uniform(0, 100, n_points)
y_coords = np.random.uniform(0, 100, n_points)

# Simulated thermal band brightness temperatures (in Kelvin)
T31 = np.random.normal(loc=300, scale=3, size=n_points)  # Band 31
T32 = T31 - np.random.normal(loc=0.5, scale=0.2, size=n_points)  # Band 32

# Simulated NDVI values
ndvi = np.random.uniform(0.1, 0.8, size=n_points)

# Emissivity estimation based on NDVI (simplified)
emissivity = np.where(ndvi < 0.2, 0.97,
              np.where(ndvi > 0.5, 0.99, 0.985))

# 2. Land Surface Temperature (LST) calculation using simplified split-window algorithm
# Basic formula (simplified version):
# LST = T31 + a * (T31 - T32) + b
# Where a and b are empirical coefficients; emissivity is applied in full model

a = 1.0
b = -0.5
lst = T31 + a * (T31 - T32) + b
lst_celsius = lst - 273.15  # Convert from Kelvin to °C

# 3. Create DataFrame
df = pd.DataFrame({
    'x_coord': x_coords,
    'y_coord': y_coords,
    'T31_K': T31,
    'T32_K': T32,
    'NDVI': ndvi,
    'Emissivity': emissivity,
    'LST_K': lst,
    'LST_Celsius': lst_celsius
})

# 4. Summary
print(df.head())

# 5. Visualization: Temperature Map (LST)
plt.figure(figsize=(10, 6))
sc = plt.scatter(df['x_coord'], df['y_coord'], c=df['LST_Celsius'], cmap='inferno', s=50)
plt.colorbar(sc, label='LST (°C)')
plt.title("Synthetic Land Surface Temperature Map")
plt.xlabel("X Coordinate")
plt.ylabel("Y Coordinate")
plt.grid(True)
plt.tight_layout()
plt.show()
