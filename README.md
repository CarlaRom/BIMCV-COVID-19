<div class="clearfix" style="padding: 0px; padding-left: 100px; display: flex; flex-wrap: nowrap; justify-content: space-evenly; align-items:center">
<a href="http://bimcv.cipf.es/"><img src="https://github.com/BIMCV-CSUSP/BIMCV-COVID-19/blob/master/chestRx/logoinst.png?raw=true"</a><a href="http://ceib.san.gva.es"></a></div>

# BIMCV-COVID-19
## For your information, the content on BIMCV github space is subject to daily updates.
Following common strategies and initiatives emerged from the scientific community at international level, a series of actions are being carried out within the Valencia Region Image Bank (BIMCV) that combines data from the [PadChest dataset](http://bimcv.cipf.es/bimcv-projects/padchest) with future datasets based on COVID-19 pathology to provide the open scientific community with data of clinical-scientific value that helps early detection of COVID-19.

Medical Imaging Example of COVID-19 Rx from [medRxiv preprint doi](https://doi.org/10.1101/2020.02.14.20023028)
![ChestRX-COVID](https://github.com/BIMCV-CSUSP/BIMCV-COVID-19/blob/master/chestRx/deepChest-covid.png)

## Goal
Collect and publish chest X-ray images, coming from hospitals affiliated to the BIMCV, to which data that allows their identification will be erased for the purpose of training Deep Learning (DL) models. Such training is meant to obtain an early detection of infection and pneumonia by Covid from a simple chest X-ray. 
In order to achieve this, these images will be structured into subgroups of images coming from the PadChest dataset with differential diagnosis related to COVID-19’s radiological semiology, allowing to develop the first models based on Artificial Intelligence to better predict and understand the infection. 
## Immediate actions to do
Our investigation group “Unidad Mixta de Imagen Biomédica FISABIO-CIPF” is working towards launching these models using the FISABIO’s BIMCV (Openmind) platform that is shared with the computational resources from CIPF. It is a series of shared computational resources to face these challenges through the TransBioNet net.
While waiting for official authorization for an extraction of a new COVID-19’s X-ray data set from the competent authorities, the next tasks/actions are being carried out, using PadChest images as basis:

* Reorganization of PadChest data set related to COVID-19’s pathology course. 
* Extraction or data organization into subgroups coming from PadChest (known in AI as Data Curation) starting with pneumonia, infiltrated and controls. 
* Effective and well-adjusted partitioning (see figure 1).
* Preprocessing. Basically, the images are gonna be stored both in cluster and Kaggle and distributed into three groups: training or (Tr) 60%, validation or (Val) 20% and test or (Te) 20%. 

Various models will be trained and the ones which obtain better accuracy will be available as open source code in order to when the new BIMCV-COVID-19 data set is acquired, enable Transfer-Learning in new computational models.

PadChest database is partitioned in ["10 fold cross validation"](https://en.wikipedia.org/wiki/Cross-validation_(statistics)#k-fold_cross-validation) following the next criteria and/or specifications:

* Count by subject and count by total partitions (Tr, Val and Te) and by gender.
* The total percentage by partition must be evenly distributed for each tag separated value (tsv) generated.

PadChest partitioned:

![partition-COVID](https://github.com/BIMCV-CSUSP/BIMCV-COVID-19/blob/master/chestRx/Partition2.png)
