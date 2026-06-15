# Depresjon-Behavioral-Profiling

To monitor depression, a multidisciplinary team of researchers affiliated with SINTEF Digital, Haukeland University Hospital (NORMENT), the University of Bergen, the University of Oslo, and the Simula Metropolitan Center for Digital Engineering in Norway.

This project explores behavioral profiling and digital phenotyping using wearable actigraphy data collected from individuals with depression, bipolar disorder, and healthy controls.

Instead of predicting diagnostic labels directly, the project focuses on discovering hidden behavioral patterns from motor activity signals using unsupervised machine learning techniques.

The goal is to identify latent behavioral profiles associated with psychiatric conditions such as depressive inactivity, circadian rhythm disruption, and irregular activity patterns.

### Dataset: 
The clinical data were collected within psychiatric research protocols and later made publicly available for machine learning analysis of motor activity patterns in depression.

Refer to the following link for the complete dataset:

🔗 https://datasets.simula.no/depresjon/

### Project Pipeline
#### 1. Data Loading
- Loaded multiple CSV files from condition and control folders
- Combined all subjects into a unified dataframe
- Assigned unique patient identifiers

#### 2. Data Preprocessing
- Converted timestamps into datetime format
- Removed invalid activity values
- Sorted data chronologically
- Applied signal smoothing using rolling averages

#### 3. Behavioral Feature Extraction
Extracted clinically meaningful behavioral signals including:
- Mean activity
- Activity variability
- Maximum movement intensity
- Inactivity ratio
- Nighttime activity
- Morning activity
- Circadian rhythm disruption

#### 4. Feature Scaling
Applied StandardScaler before clustering to normalize feature magnitudes.

#### 5. Behavioral Clustering
Used:
- KMeans clustering
- Silhouette score optimization
- PCA dimensionality reduction to identify latent behavioral groups.

### Key Findings
The clustering results revealed distinct behavioral profiles such as:
- Stable high-activity profiles
- Low-energy depressive-like behavior
- Irregular circadian activity patterns
- Nocturnal activity disruption
The results suggest that wearable movement signals can capture meaningful behavioral differences associated with mental health conditions.

### Technologies Used
- Python
- Pandas
- NumPy
- Scikit-learn
- Seaborn
- Matplotlib

### Future Improvements
- Deep learning sequence models (LSTM / Transformers)
- Temporal clustering
- Sleep-stage analysis
- Real-time behavioral monitoring
- Multimodal wearable integration
