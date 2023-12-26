

### 1. Dataset

Source code: [here](https://github.com/twelfthywn/NaturalDisasterForecastingSystem/blob/main/src/data_collection.ipynb)

- Bộ dữ liệu gốc: *Global Landslide Catalog* 

  Nguồn: [here](https://data.nasa.gov/Earth-Science/Global-Landslide-Catalog-Export/dd9e-wu2v)

- Dữ liệu thu thập thêm:

  -  [Thời tiết](https://www.visualcrossing.com/weather-api)
  -  [Độ cao](https://developers.airmap.com/docs/elevation-api)
  -  [Châu lục](https://pypi.org/project/pycountry-convert/)
  -  [Mùa](https://www.nationalgeographic.org/encyclopedia/season/)
  -  [Mật độ dân số](https://sedac.ciesin.columbia.edu/data/set/gpw-v4-population-density-rev11/)
  -  [Độ che phủ rừng](https://data.globalforestwatch.org/documents/134f92e59f344549947a3eade9d80783/e%20xplore/)
  -  [Kết cấu của đất](https://developers.google.com/earth%02engine/datasets/catalog/OpenLandMap_SOL_SOL_TEXTURE%02CLASS_USDA-TT_M_v02)

### 2. Data preprocessing

Source code: [here](https://github.com/twelfthywn/NaturalDisasterForecastingSystem/blob/main/src/data_preprocessing.ipynb)

Các bước tiền xử lý bao gồm: xử lý các thuộc tính dạng *datetime*, loại bỏ các cột chứa thông tin không cần thiết, và xử lý missing values.

### 3. EDA

Source code: [here](https://github.com/twelfthywn/NaturalDisasterForecastingSystem/blob/main/src/EDA.ipynb)

Các bước phân tích thăm dò bao gồm: thống kê mô tả, phân tích trực quan dữ liệu theo thời gian (time series), phân tích tổng hợp thuộc tính, phân tích trực quan trên bản đồ địa lý.

### 4. Feature selection, Feature engineering and Model development

Source code: [here](https://github.com/twelfthywn/NaturalDisasterForecastingSystem/blob/main/src/model_development.ipynb)

#### Feature selection

Các thuộc tính được lựa chọn để đưa vào mô hình dựa vào kết quả sau khi phân tích thăm dò, kết hợp với hai phương pháp thống kê là *One way ANOVA* và *Chi-square test*.

#### Feature engineering

Các kỹ thuât để biến đổi dữ liệu trước khi đưa vào mô hình bao gồm: kết hợp các nhóm thuộc tính có độ tương quan cao, kết hợp và mã hóa các cột chứa thông tin mô tả (text description), mã hóa one-hot cho các thuộc tính phân loại, và feature scaling.
