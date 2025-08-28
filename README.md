# Projects Repository
## Collection of data science projects

Retail Time Series Forecasting:

This project focuses on forecasting daily operational costs using over three years of historical data (~1M records). I built a regression model in Python with XGBoost and scikit-learn, engineering 18 time-based features (such as day-of-week, lag values, and rolling averages) to capture trends and seasonality.

The workflow included extensive data cleaning and exploratory data analysis with pandas, NumPy, and matplotlib to handle missing values, remove outliers, and uncover key patterns in the dataset. 

The final model achieved strong predictive performance, with an average R² of 0.90 and RMSE of 416.16, significantly outperforming baseline estimates
---------------------------------------------------------------------------------------------------------------------------------------------------

Object Detection Model (collaborative project):

This project applies YOLOv8s to detect common road objects such as cars, trucks, buses, traffic lights, and road signs. The model was trained on the BDD100K dataset (via Kaggle) with extensive data augmentation (geometric adjustments, flipping, color shifts, copy-paste, etc.) to improve generalization across varied conditions. Training ran for 300 epochs, with a learning rate schedule decaying from 0.0007 to 0.0001.

To evaluate performance across domain shifts, we tested the model on both:

- Still images from around Bowling Green, OH.

- Live inference via webcam capture, running predictions on local environments in real time.

Training metrics demonstrated effective convergence, with total loss stabilizing around 2.0. Component analysis showed classification loss dominating early but decreasing steadily alongside box and DFL losses. Performance metrics revealed a precision peak of 0.73 (epoch 40) followed by a trade-off with recall, which improved from 0.35 to 0.48 over training.

These results highlight YOLOv8’s strong capacity for learning road object detection, while also illustrating the challenges of balancing precision and recall under domain shift conditions

The source code for this project can be found at this repository: https://github.com/EvanSluterbeck/ExploringYOLOForAccurateObjectDetection
