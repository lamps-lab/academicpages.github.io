---
permalink: /project/
author_profile: true
redirect_from: 
  - /project
---

Metadata Extraction from scanned ETDs
======
Extracting metadata from scholarly papers is an important text mining problem. Widely used open-source tools such as GROBID are designed for born-digital scholarly papers but often fail for scanned documents, such as Electronic Theses and Dissertations (ETDs). We have implemented heuristic model to extract seven metadata fields from the cover pages of scanned ETDs. We are also conducting research on learning based classification method such as Conditional Random Field (CRF) to extract the metadata. The process generally starts with converting scanned pages into images and then text files by applying Optical Character Recognition (OCR) tools. However, extracting metadata and full text segmentation from scanned ETDs are challenging due to poor image resolution, imperfection of OCR techniques, and typewritten text. Thus, another part of this research invloves in experimentation of various open-source and commercial based OCR tools including tesseract-OCR, Google Cloud API, and Clova.

**Heuristic Approach to Extract Metadata**


Although many complicated learning-based models could be built (e.g., CRF or Support Vector Machine (SVM)), to the best of our knowledge we could not find any dedicated effort and evaluation of heuristic methods with the ETD task. Heuristic methods are generally faster, suitable for capturing evident patterns. For this task, we carefully analyzed 100 scanned ETDs from MIT and Vtech libraries, and designed regular expressions for extracting seven metadata fields: titles, authors, years, degrees, academic programs, institutions, and advisors. Our model achieved an accuracy up to 97% and posed a strong baseline for further study on learning based methods.
<div style="text-align: justify;">
<br /></div>
<table align="center" cellpadding="0" cellspacing="0" class="tr-caption-container" style="margin-left: auto; margin-right: auto; text-align: center;"><tbody>
<tr><td style="text-align: center;"><a href="/images/flowchart-ETDMiner.png" style="margin-left: auto; margin-right: auto;"><img border="0" data-original-height="833" data-original-width="949" height="560" src="/images/flowchart-ETDMiner.png" width="640" /></a></td></tr>
<tr><td class="tr-caption" style="text-align: center;"><span style="font-size: 12.8px;">Figure-1: Metadata Extraction Framework</span></td></tr>
</tbody></table>

**Learning Based Approach to Extract Metadata**
----

Currently, this research is on-going. We made a significant progress on this task and implemented CRF model with 13 features.

OCR
======
**Tesseract-OCR**

