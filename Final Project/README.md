# Minnesota Corn Growers App
![GitHub last commit](https://img.shields.io/github/last-commit/TzuYuMa/Corn?style=for-the-badge)

## Overview  
This app aims to provide Minnesota corn growers with updated information on growing degree days (AGDD), soil moisture, and reference evapotranspiration (ET). Selecting the desire area to download data with CSV or PDF file, or you can find the [Data URLs for GeoJson](#data-urls-for-geojson) Utilizing GeoJSON format from APIs. This supports agricultural decision-making in Minnesota by facilitating the comparison of various interpolation models for accurate analysis.

## Objectives  
- Develop a system to calculate and map AGDD, ET, and soil moisture for Minnesota Corn Growers.
- Utilize local and cloud computing to automate data processing from collection through spatial visualization via ArcOnline.
- Ensure data accuracy and seamless integration of varied datasets within a PostgreSQL database.
- Maintain user-friendly access and support real-time updates.

## Data URLs for GeoJson
- AGDD: 
  ```python
  https://googlecloudrun-nvrttyom5q-uc.a.run.app/agdd/minnesota
  ```
  In the app, we offer data for the previous growing season, spanning from **April 2023 to September 2023**. We employed Inverse Distance Weighted (IDW) interpolation to extrapolate data from 153 observation sites across the entirety of Minnesota.

  Our Accuracy Assessment concluded that IDW provided the most dependable results.
- ET: [[ET Data URL](https://googlecloudrun1-ubtvfytuvq-uc.a.run.app/et_points)]
- Soil Moisture:
  ```python
  https://googlecloudrun-nvrttyom5q-uc.a.run.app/soil_moisture/<date>
  ```
  Please manually replace `<date>` with the desired year and month in your browser's address bar


  Available date range: 20237-20244 (July 2023 - April 2024)

  For example:
  
  ```plaintext
  https://googlecloudrun-nvrttyom5q-uc.a.run.app/soil_moisture/20237
## Data Sources 
- **IEM**: Daily Min/Max temperature data.
- **NASA SMAP**: Soil Moisture.
- **TerraClimate**: Actual Evapotranspiration.
  
## Contributors 
- Samikshya Subedi
- Tzu-Yu Ma  

