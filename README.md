# FIR_Dataset

First Hybrid (Handwritten + Printed) semi-structure document analysis dataset consists on Indian legal documents (First Information Report). This is Dataset for the paper **"TransDocAnalyser: A framework for semi-structured offline handwritten documents analysis with an application to legal domain"**, accepted(**Oral**) and to be published at The 17th International Conference on Document Analysis and Recognition , August 21-26, 2023 — San José, California, USA.

## About

![intro_image](https://drive.google.com/uc?id=1JWP-WAtr5Glo_fCiGGeKnN1zom3ZvCfX&export=download) 


First Information Report (FIR) documents contain details about incidents of cognisable offence, that are written at police stations based on a complaint.
FIRs are usually filed by a police official filling up a printed form; hence the documents contain both printed and handwritten text. This Dataset consists of FIR documents written at police stations in India. 

FIR contains many fields including the name of the complainant, names of suspected/alleged persons, statutes that may have been violated, date and location of the incident, and so on. In this work, we selected four target fields from FIR documents for the data annotation and recognition task –
          (1) **Year** (the year in which the complaint is being recorded), 
          (2) **Complainant’s name** (name of the person who lodged the complaint), 
          (3) **Police Station** (name of the police station that is responsible for investigating the particular incident),and 
          (4) **Statutes** (Indian laws that have potentially been violated in the reported
          incident; these laws give a good indication of the type of the crime). 

We selected these four target fields because we were able to collect the gold standard for these four fields from some of the police databases. Also, digitizing these four
fields would enable various societal analysis, such as analysis of the nature of crimes in different police stations, temporal variations in crimes, and so on.
