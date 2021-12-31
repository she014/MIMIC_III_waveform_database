# MIMIC-III Waveform Database Matched Subset
This repository is used to demonstrate how to use MIMIC-III waveform database for continuous blood pressure estimation.\
I am working on continuous cuffless blood pressure estimation. There are just few databases which includes long-term Electrocardiogram (ECG), Photoplethysmogram (PPG) and blood pressure (BP) waveforms. And MIMIC-III database is the largest one with several different physiological signals which is great for cuffless BP estimation research or it can be used for benchmark of researches of this kind. The one used and demonstrated here is [MIMIC-III Waveform Database Matched Subset](https://physionet.org/content/mimic3wdb-matched/1.0/). This database contains 22,317 waveform records, and 22,247 numerics records, for 10,282 distinct ICU patients. These recordings typically include digitized signals such as ECG, ABP, respiration, and PPG, as well as periodic measurements such as heart rate, oxygen saturation, and systolic, mean, and diastolic blood pressure. This database is a subset of the MIMIC-IIIWaveform Database, representing those records of which the patient has been identified, and their corresponding clinical records are available in the MIMIC-III Clinical Database [^1]. This is great if you need detailed information from a patient, for example. the height and weight, gender, hypertension or not... For more information of MIMIC-III clinical database, please refer [MIMIC-III Clinical Database](https://physionet.org/content/mimiciii/1.4/).

Some explanition of this database and the usage of it can be found on the webpage of the database. However, I found it is not clear enough, so I will describe my steps to use this database and the problems and solutions I experienced.

![](/images/github1.png)

As it can be seen that the total uncompressed size of this dataset is **2.4 TB** which makes it almost impossible to download them all locally. I will save them to my external hard drive. Now I will explain how to download the dataset. As shown in the **Figure**, there are three ways to download the database, I use the third one. First, you need to install **wget** on your machine, based on what operating system you are using, the process may be different. I am using Windows system, so you can directly download **wget** from this [website](http://gnuwin32.sourceforge.net/packages/wget.htm). Tutorials can be found online demonstates the process step by step, you cannot get it wrong. After installing wget, let's start to download.

1. Open windows command window. And redirect to the path where you want to save these files. I will save them to my hard drive which is F: on my laptop. Then I create a new forlder and name it mimic3_waveform. So I redirect to this folder in command window.

![](/images/github2.jpg)

2. Copy and paste the wget command from the webpage, and then add which folder you want to download. Let's say p01. Just like shown below. And then you probabliy can find there is an error says "cannot verify physionet.org's certificate" and it also suggests "to connect to physionet.org insecurely, use '--no check-certificate'". So let's just add this into our command. Then click **Enter**, it should start downloading, and just wait it will take some time to download such a large database.

![](/images/github3.jpg)
![](/images/github4.jpg)

3. When you see this, means the downloading is in process. And you can check there is a p01 folder created in your destination folder and there are tons of folders are created for each subject. I downloaded p00 part, it used about 10 hours, it depends on your internet and machine speed. The p00 part is about 250GB large. So I will process this part and only keep the parts I can use for my work and delete for the next part.

![](/images/github5.jpg)


[^1]: Moody, B., Moody, G., Villarroel, M., Clifford, G., & Silva, I. (2020). MIMIC-III Waveform Database Matched Subset (version 1.0). PhysioNet. https://doi.org/10.13026/c2294b.
