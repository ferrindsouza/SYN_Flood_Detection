# Detecting SYN Flood Attacks Using ML Algorithms

This project explores the use of Machine Learning (ML) techniues to detect SYN FLood attacks, a type of Denial-of-Service (DoS) attack.
By leveraging data collected from network traffic under both normal and attack scenarios, the project aims to train and evaluate ML models (including anomaly detection algorithms) to determine which algorithms are best suited for detecting such attacks. 


## Project Features

1. **Front-End for Data Collection**:
    - Created 4 VMs each of which has a role. The 3 VMs which run Linux OS will act as the normal user at one instance and malicious user at another instance and the 4th VM will be the main server as shown in the diagram below:
    ![alt text](image.png)
    - Developed a simple interface for collecting network traffic (index.html) by creating a form asking for user name, email and message. This form has been created on an Apache server.

2. **Dataset Creation**:
    - In order to generate normal traffic macros was used which helped automate the process of filling forms by giving sufficient gap between each time the form was filled to mimic normal user activity.
    - In order to generate a SYN Flood attack hping3 cmd was used from one VM targetting the other in order to mimic a typical SYN Flood attack.

3. **Machine Learning Model Training**:
    - Trained multiple ML models using the datasets, including:
        - Supervised learning algorithms like Decision Trees, Random Forests, and Support Vector Machines (SVM).
        - Deeep Learning models for more compplex pattern recognition.
    - Evaluated ML models based on accuracy, precision, recall, and F1-score to identify the best performing approach.

4. **Model Evaluation and Comparison**:
    - Compared the effectiveness of the trained modelsin detecting SYN Flood Attacks
    Analysed strengths and weaknesses of each model to provide insights into their suitability for real-world deployment.


## Technologies Used

- **Virtual Machines**:  Set up using VMware
- **Frontend development**: Built using HTML, CSS, iMacros extension
- **Networking Tools**: Wireshark, tcpdump
- **Machine Learning Frameworks**: 
    - Python libraries such as Scikit-learn
- **Data Processing**: Pandas, NumPy, for preprocessing and feature extraction

## Getting Started

### Prerequisites

- Virtualization Software (e.g., VMware, VirtualBox)
-  Python 3.8+ and relevant libraries
- iMacros pluggin for a web browser. For the purposes of this experiment ran it on Mozilla Firefox.
- Basic understanding of TCP/IP networking and ML algorithms.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/ferrindsouza/SYN_Flood_Detection.git```

2. Set up the VMs ( make sure they're on the same network) and install required tools for network monitoring

3. Install the Pythton dependencies 
    ```bash 
        pip install -r requirements.txt```

## Data Collection
    - Followed the steps mentioned in Dataset Creation
    - Monitored the traffic on wireshare and saved it in an .cap file fir further analysis.

## Training ML Models
    - Preprocess the collected data to extract relevant features
    - Train the ML models using various ML algorithms
    - Evaluate the models and generate reports

## Results and Findings
    - MLP has been shown to be the most effective algorithm in detecting SYN Flood based on this experiment. THis shows anomaly detection algorithms are most suitable to detect SYN FLood Attacks.
    - Insights into feature importance and challenges in distinguishing normal and attack traffic.

## Future Work
    - Extend the detection system to other types of DoS/DDoS attacks.
    - Implementing real-time detection using trained models.


## Contributors
    Ferrin Dsouza



 