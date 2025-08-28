Projects

A collection of projects I've worked on (solo and collaborative). Each project lives in its own repository, linked below.

Time Series Forecasting Project:

This project focuses on forecasting daily operational costs using over three years of historical data (~1M records). I built a regression model in Python with XGBoost and scikit-learn, engineering 18 time-based features (such as day-of-week, lag values, and rolling averages) to capture trends and seasonality.

The workflow included extensive data cleaning and exploratory data analysis with pandas, NumPy, and matplotlib to handle missing values, remove outliers, and uncover key patterns in the dataset.

The final model achieved strong predictive performance, with an average R² of 0.90 and RMSE of 416.16, significantly outperforming baseline estimates.

Repository: https://github.com/EvanSluterbeck/Projects

Object Detection with YOLOv8:

This project applies YOLOv8s to detect common road objects such as cars, trucks, buses, traffic lights, and road signs. The model was trained on the BDD100K dataset (via Kaggle) with extensive data augmentation (geometric adjustments, flipping, color shifts, copy-paste, etc.) to improve generalization across varied conditions. Training ran for 300 epochs, with a learning rate schedule decaying from 0.0007 to 0.0001.

To evaluate performance across domain shifts, we tested the model on both:

Still images from around Bowling Green, OH.

Live inference via webcam capture, running predictions on local environments in real time.

Training metrics demonstrated effective convergence, with total loss stabilizing around 2.0. Component analysis showed classification loss dominating early but decreasing steadily alongside box and DFL losses. Performance metrics revealed a precision peak of 0.73 (epoch 40) with a trade-off as recall gradually improved from 0.35 to 0.48.

Repository: https://github.com/EvanSluterbeck/ExploringYOLOForAccurateObjectDetection
