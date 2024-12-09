# Versions

## Introduction
This section details the characteristics of different dashboard versions implemented in static web pages and Python applications hosted on Amazon Web Services (AWS), describing their particularities, technologies used, and evolution.

## Dashboard Versions

### Version 1: Basic Implementation

#### Key Features
- **Technologies**: 
  - HTML5
  - CSS3
  - fontawesome
  - Vanilla JavaScript
  - Amcharts4
  - jQuery
  - Bootstrap 3.3.6 
  - ArcGIS API for JS  4.14
  - DataTables JS



## Architecture

- Completely static web page on **AWS S3**
- Hardcoded content directly in HTML and JavaScript files
- Responsive design using Bootstrap
- Interactivity implemented with Amcharts4, ArcGis for JavaScript
- No consumption of external data files

#### Directory Structure
```
/v1
├── login.html
├── index.html
├── some_pages.html
├── map/
│   └── index.html
├── data_js/
│   └── files.js
├── vendors/
│   └── style.css
│   └── some_assets/
└── images/
    └── files
```

### Version 2: Data Consumption Enhancement

- **Technologies**: 
  - HTML5
  - CSS3
  - Vanilla JavaScript
  - Amcharts4
  - jQuery
  - Bootstrap 5
  - Python3
  - Pandas, GeoPandas, Numpy, Shapely, re,
  - ArcGIS for JS
  - Plotly JS
  - DataTables JS



#### Main Characteristics

 - Built upon Version 1 with significant improvements
 - External JSON file consumption
 - UX/UI improvements
 - Data and presentation separation

## Architecture

- Maintains the base structure of Version 1
- Capabilities for render Polygons
- Introduces JSON files for:
  - Data storage
  - Dynamic content loading
- Dynamic rendering based on JSON data

#### Directory Structure
```
/v2
├── login.html
├── index.html
├── map.html
├── cycle_section/
|    └── index.html
├── css/
│   └── style.css
├── js/
│   └── section.js
|   └── section.json
└── some_assets/
    └── files

```

### Version 3: Advanced Web Application (Experimental)

#### Key Features
- **Infrastructure**: EC2 instance with Ubuntu 22.04 LTS  
- **Primary Language**: Python3  
- **Web Framework**: Streamlit  
- **UX Focus**: Minimalist and functional design  

#### Arquitectura

##### Analysis and Visualization Libraries

- **Data Processing**
  - Pandas
  - NumPy
  - GeoPandas

- **Visualization**
  - Plotly
  - Streamlit (for rendering charts)

#### Directory Structure
```
experimental-app/
├── app/
│   ├── home.py             # App
│   ├── tools/
│   │    └── preparer_data.ipynb  # Preprocess data
│   │  
│   ├── pages/
│   │   └── section.py/  # section pages
├── src/                  #some assets
├── data/
│   ├── files.csv          
│   └── files.geojson          
├── requirements.txt        # Libraries
├── venv/                   # virtual enviroment
└── .gitignore              # Variables de entorno
```



#### Minimalist UX Characteristics

##### Design Principles

- Clean interface without distractions
- Use of neutral colors
- Clear and legible typography
- Focus on content and functionality
- Streamlit components for rapid design

##### Typical Streamlit Application Structure

- Sidebar for configurations
- Main area for visualizations
- Minimalist interactive components
- Dynamic data loading


#### Best Practices

##### Development  
- Use version control (Git)  
- Document configurations  
- Keep requirements.txt up to date  

##### Performance

- Optimize data loading
- Use Streamlit cache
- Process data in batches


##### Additional Notes

- Flexibility to add more functionalities
- Easy integration with other data sources
- Rapid prototyping of analyses and visualizations