Hello everyone! My name is Evan Sluterbeck and will be graduating from Bowling Green State University in December. I am studying Computer Science with a Computational Data Science Specialization. I am passionate about all things with data: Data Science, Data Enginnering, Data Analytics; and I am actively seeking full-time positions in any of these roles. 

My Projects: This is a collection of projects I've worked on (solo and collaborative). Most of my solo projects should live in this current repo (EvanSluterbeck/Projects), but I have linked the respective repository for each project.

Time Series Forecasting Project (Solo):

This project focuses on forecasting daily operational costs using over three years of historical data (~1M records). I built a regression model in Python with XGBoost and scikit-learn, engineering 18 time-based features (such as day-of-week, lag values, and rolling averages) to capture trends and seasonality.

The workflow included extensive data cleaning and exploratory data analysis with pandas, numpy, and matplotlib to handle missing values, remove outliers, and uncover key patterns in the dataset.

The final model achieved strong predictive performance, with an average R² of 0.89 and RMSE of 527.44, significantly outperforming baseline estimates.

Repository: https://github.com/EvanSluterbeck/Projects

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Object Detection with YOLOv8 (Collaborative):

This project applies YOLOv8s to detect common road objects such as cars, trucks, buses, traffic lights, and road signs. The model was trained on the BDD100K dataset (via Kaggle) with extensive data augmentation (geometric adjustments, flipping, color shifts, copy-paste, etc.) to improve generalization across varied conditions. Training ran for 300 epochs, with a learning rate schedule decaying from 0.0007 to 0.0001.

To evaluate performance across domain shifts, we tested the model on both:

- Still images from around Bowling Green, OH.

- Live inference via webcam capture, running predictions on local environments in real time.

Training metrics demonstrated effective convergence, with total loss stabilizing around 2.0. Component analysis showed classification loss dominating early but decreasing steadily alongside box and DFL losses. Performance metrics revealed a precision peak of 0.73 (epoch 40) with a trade-off as recall gradually improved from 0.35 to 0.48.

Repository: https://github.com/EvanSluterbeck/ExploringYOLOForAccurateObjectDetection

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Parallel K-Means Clustering with MPI (Collaborative)

This project implements a parallel version of Lloyd’s K-means algorithm using C++ and Boost.MPI. We scaled a 1,000,000-sample, 25-feature dataset across multiple processes, starting from a serialized baseline and building a distributed system that maintains full correctness and reproducibility.

Our design uses MPI collective operations (broadcast, all_reduce) for centroid updates and convergence checks, with each process performing local point assignments and contributing to global reductions. We ran 10 deterministic trials per configuration (1–10 processes), enabling detailed performance and scalability analysis.

Key Features:

Balanced data distribution across all MPI processes

Deterministic seeding for reproducible serial/parallel comparisons

Verified identical cluster assignments and centroid values across all configurations

Near-linear scaling: 9.76× speedup on 10 processes with >95% efficiency

Includes Slurm job scripts, timing utilities, plots, and a full performance report

Repository: https://gitlab.com/Shafern01/cs4170_fa2025_a03_g02

