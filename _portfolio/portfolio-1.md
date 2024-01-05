---
title: "Table Detection & Structure Recognition"
excerpt: "An innovative approach to OCR of tables in documents, focusing on Table Detection and Structure Recognition, with the development of a robust Table Extraction Pipeline. Significant progress in Transformer-based model pruning enhances efficiency without compromising accuracy.<br/><img src='/images/500x300.png'>"
collection: portfolio
---

Capstone project 'Detection, Recognition, and Extraction of Table Structure Data,' supervised by Assoc. Prof. Quản Thành Thơ Ph.D. and Mr. Băng Ngọc Bảo Tâm M.Eng., carried out by students Nguyễn Luật Gia Khôi and Phạm Bùi Minh Huân at the Ho Chi Minh City University of Technology&#8203;``【oaicite:8】``&#8203;. The project addresses the growing need for efficient document digitization, particularly focusing on the extraction of structured table data from PDFs or images into spreadsheets&#8203;``【oaicite:7】``&#8203;.

The core problems tackled include the development of a deep learning system for detecting and recognizing tables in documents and implementing a parameter pruning method for Transformer-based models. This approach significantly reduces the number of parameters without sacrificing model accuracy, leading to a more efficient and effective processing pipeline&#8203;``【oaicite:6】``&#8203;.

Experimental evaluations of various Table Detection (TD) models were conducted, utilizing both public and private datasets. These datasets included manually labeled financial statements, receipts, and inventory management tables, among others&#8203;``【oaicite:5】``&#8203;. Evaluation metrics such as recall, precision, and F1-score across different Intersection over Union (IoU) thresholds were used&#8203;``【oaicite:4】``&#8203;.

Key findings from these experiments include:
- CDeCNet achieved the highest precision and F1-score at all thresholds.
- DETR and CascadeTabNet also showed high precision, while Cascade Mask RCNN trained on TNCR displayed the highest recall.
- Notably, no single model completely outperformed the others&#8203;``【oaicite:3】``&#8203;.

The CDeCNet model, despite its high precision, had a significantly larger number of parameters, leading to slower inference times. In contrast, the DETR model, based on a Transformer architecture, had the smallest number of parameters and was efficient in accommodating variable numbers of objects&#8203;``【oaicite:2】``&#8203;.

A standout achievement of this project was the development of a pruning method for Transformer-based models. This method outperformed traditional uniform pruning techniques, reducing the model's parameters up to 66% while only experiencing a minimal drop in performance (2% - 4.3% in AP and AR; 1% in GriTS_Top) &#8203;``【oaicite:1】``&#8203;.

Overall, the project successfully built a modular, lightweight pipeline for various table types and domains, significantly advancing the field of table OCR. It laid the groundwork for future research, particularly in improving pre- and post-processing methods and further developing pruning techniques for Transformer-based models&#8203;``【oaicite:0】``&#8203;.
