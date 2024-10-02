# NSL-KDD DATASET
The KDD cup was an International Knowledge Discovery and Data Mining Tools Competition. 
In 1999, this competition was held with the goal of collecting traffic records. 
The competition task was to build a network intrusion detector, a predictive model capable of distinguishing between “bad’’ connections, 
called intrusions or attacks, and “good’’ normal connections. 
As a result of this competition, a mass amount of internet traffic records were collected and bundled into a data set called the KDD’99, 
and from this, the NSL-KDD data set was brought into existence, as a revised, cleaned-up version of the KDD’99 from the University of New Brunswick.

These data sets contain the records of the internet traffic seen by a simple intrusion detection network and are the ghosts of the traffic encountered by a real IDS 
and just the traces of its existence remains. 
The data set contains 43 features per record, with 41 of the features referring to the traffic input itself and
the last two are labels (whether it is a normal or attack) and Score (the severity of the traffic input itself).

# Attacks

Within the data set exists 4 different classes of attacks: Denial of Service (DoS), Probe, User to Root(U2R), and Remote to Local (R2L).

dos - flooding network with large traffic so that network has to be shutdown and unable to access by others
probe - steal info from network
u2r - start from normal user and tried to get access of root user
r2l - try to get local access to remote machine

Breakdown of subclasses of each attack --

dos = ['apache2','back','land','neptune','mailbomb','pod','processtable','smurf','teardrop','udpstorm','worm']
probe = ['ipsweep','mscan','nmap','portsweep','saint','satan']
u2r = ['buffer_overflow','loadmodule','perl','ps','rootkit','sqlattack','xterm']
r2l = ['ftp_write','guess_passwd','http_tunnel','httptunnel','imap','multihop','named','phf','sendmail','snmpgetattack','snmpguess','spy','warezclient','warezmaster','xlock','xsnoop']

Dataset is highly biased towards dos attack and normal request. Highly imbalanced data

Train dataset Attack
dos       45927
normal    67343
probe     11656
r2l         995
u2r          52

Test dataset Attack
attack
dos       45927
normal    67343
probe     11656
r2l         995
u2r          52

# Features

The feature types in this data set can be broken down into 4 types:

4 Categorical (Features: 2, 3, 4, 42)
6 Binary (Features: 7, 12, 14, 20, 21, 22)
23 Discrete (Features: 8, 9, 15, 23–41, 43)
10 Continuous (Features: 1, 5, 6, 10, 11, 13, 16, 17, 18, 19)


# Models Tried and Achieved accuracy and recall on test data

Multinomial Naive Bayes--------------------Accuracy = 74.45---------Recall = (0.55)
Logistic Regression (cross-entropy loss)---Accuracy = 74.5
Bernoulli Naive Bayes----------------------Accuracy = 76.7
Support Vector Classifier------------------Accuracy = 
Random Forest Classifier
Deep Learning model
