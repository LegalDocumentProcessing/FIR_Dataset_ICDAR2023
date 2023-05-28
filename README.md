# FIR_Dataset

First Hybrid (Handwritten + Printed) semi-structure document analysis dataset consists on Indian legal documents (First Information Report). This is Dataset for the paper **"TransDocAnalyser: A framework for semi-structured offline handwritten documents analysis with an application to legal domain"**, accepted(**Oral**) and to be published at The 17th International Conference on Document Analysis and Recognition , August 21-26, 2023 — San José, California, USA.

## About

![intro_image](https://drive.google.com/uc?id=1JWP-WAtr5Glo_fCiGGeKnN1zom3ZvCfX&export=download) 


First Information Report (FIR) documents contain details about incidents of cognisable offence, that are written at police stations based on a complaint.
FIRs are usually filed by a police official filling up a printed form; hence the documents contain both printed and handwritten text. This Dataset consists of FIR documents written at police stations in India. 

FIR contains many fields including the name of the complainant, names of suspected/alleged persons, statutes that may have been violated, date and location of the incident, and so on. In this work, we selected four target fields from FIR documents for the data annotation and recognition task : \

```
  - category_id: 0
      - Police Station : Name of the police station that is responsible for investigating the particular incident  
  - category_id: 1
      - Year : The year in which the complaint is being recorded.
  - category_id: 2
      - Statutes : Indian laws that have potentially been violated in the reported incident; these laws give a good indication of the type of the crime. 
  - category_id: 3
      - Complainant’s name:  Name of the person who lodged the complaint.  
```
## Citation
If you use this dataset , please refer to the following paper:
```
  @inproceedings{sagar2023fir,
   author = {Chakraborty, Sagar and Harit, Gaurav and Ghosh, Saptarshi},
   title = {{TransDocAnalyser: A Framework for Offline Semi-structured Handwritten Document Analysis in the Legal Domain}},
   booktitle = {{Proceedings of the 17th International Conference on Document Analysis and Recognition (ICDAR)}},
   year = {2023}
  }
 ```
## Dataset and Annotation

FIR dataset is consists of 544 annotated images. There are total 2447 annotations. The dataset json contains around four annotated key text fields, such as Police Station, Year, Statutes and Complainant's name for each FIR image. All the images are of 740 X 1180 pixels.

For FIR OCR task, each image in the dataset is annotated with text bounding boxes ("bbox") and the transcript of each text bbox("text"). Locations are annotated as rectangles with four coordinates, which are the start points (Xmin, Ymin) and the end point(Xmax, Ymax). 

```
{
"image_id": Unique index for each image,
"bbox": [
    Xmin,
    Ymin,
    Xmax,
    Ymax
],
"category_id": Name of the entity,
"image_name": Image File Name,
"text": Text value inside the bounding box
}
```

## Task

The FIR dataset can be used for 3 kinds of document analysis tasks:

    1) Text Localisation: The aim of this task is to accurately localize texts with 4 vertices.

    2) Handwritten Recognition (HWR): The aim of this task is to accurately recognize the handwritten text in a images. 

    3) Key Information Extraction : The aim of this task is to extract texts of a number of key fields from given FIR documents such as Year, Police Station, Complainant's Name and statutes

