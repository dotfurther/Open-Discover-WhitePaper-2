# Case Study #2: Open Discover® Workflow Management System's (WMS) Document Processing Performance on a Single Desktop PC


## 140 GB/hour processing rate based on collection (matter) end-to-end processing time on a single desktop PC
The end-to-end processing time includes:
- Container extraction
- Document text, metadata, language identification, embedded object/attachment extraction
- PII/PHI/FERPA entity extraction
- De-Nist of all documents
- Deduplication of all documents
- Lucene index creation
- Load file creation (document and entity Relativity Dynamic Object (RDO) load files)

### Processed Collection (Matter) for this Study:
- Digital Corpora "Govdocs1" open-source dataset of nearly 1 million freely redistributable files
- "Govdocs1" is 1000 ZIP (.zip) files, each with 1000 files.
- "Govdocs1" total ZIP file size: 310.5 GB in size.
- "Govdocs1" is 8 million documents and attachments expanded after processing.
- "Govdocs1" 1 TB expanded size after processing all containers, attachments, and embedded documents (see Image 1)
- Executable and other 'junk' file types were NOT excluded from processing. 
- OCR was not enabled for this study because OCR performance is based on how many OCR engines licensed or if user uses a web based OCR API. This case study is about raw processing performance without OCR; however, dotFurther's WMS has a very scalable solution for OCR. 

### AMD 16-core/128 GB RAM Desktop Workstation Configuration:
- Workflow Managment System (WMS) installed. WMS is a tasking based document processing/extraction/OCR system.
- 2 WMS Processing/OCR Workers (a WMS Worker is a multi-threaded document processing/extraction/OCR engine)
- SQL Server (storgage for WMS project/collection databases)
- RabbitMQ (used for tasking messages shared between WMS and Workers


