# Case Study #2: Open Discover® Workflow Management System's (WMS) Document Processing Performance on a Single Desktop PC
For Microsoft Azure performance case study see:  https://github.com/dotfurther/Open-Discover-WhitePaper-1

## Nearly 140 GB/hour processing rate based on collection (matter) end-to-end processing time on a single desktop PC
The end-to-end processing time includes:
- Container extraction
- Document text, metadata, language identification, embedded object/attachment extraction
- PII/PHI/FERPA entity extraction
- De-Nist of all documents
- Deduplication of all documents
- Load file creation (document and entity Relativity Dynamic Object (RDO) load files)

### Processed Collection (Matter) for this Study:
- Digital Corpora "Govdocs1" open-source dataset of nearly 1 million freely redistributable files
- "Govdocs1" is 1000 ZIP (.zip) files, each with 1000 files.
- "Govdocs1" total ZIP file size: 310.5 GB in size.
- "Govdocs1" is 8 million documents and attachments expanded after processing.
- "Govdocs1" 1 TB expanded size after processing all containers, attachments, and embedded documents (see Image 1)
- Executable and other 'junk' file types were NOT excluded from processing. 
- OCR was not enabled for this study because OCR performance is based on how many OCR engines licensed or if user uses a web based OCR API. This case study is about raw processing performance without OCR; however, dotFurther's WMS has a very scalable solution for OCR.
- "Govdocs1" is one of many QA tests that dotFurther runs before approving a new release.

### Desktop PC Configuration:
- AMD Ryzen 9 5950X 16-Core Processor (3.40 GHz)
- 128 GB RAM
- Windows 11 Pro
- Workflow Managment System (WMS) installed. WMS is a tasking based document processing/extraction/OCR system.
- 2 WMS Processing/OCR Workers (a WMS Worker is a distributable multi-threaded document processing/extraction/OCR engine)
- SQL Server (storgage for WMS project/collection databases)
- RabbitMQ (used for tasking message communication between WMS and Workers)

### Processing Summary Results:
|||
|---	|---	|
|Collection (Matter) input document and container size:      |310.5 GB |
|Total expanded document size after processing:              |1.09 TB |
|Collection (Matter) input document and container count:     |1,000 ZIP files |
|Total expanded document count after processing:             |8,008,540 |
|Total original document count:                              |4,622,569 | 
|Total excluded document count:                              |0 | 
|Total empty (zero-byte) document count:                     |1,138,239 | 
|Total container unextractable document count:               |1 | 
|Total NIST document count:                                  |478,585 |
|Total elapsed processing time (end-to-end):                 |7.88 hours|
|Expanded document processing rate:                          |137.95 GB/hour|

See Image 1 for a WMS processing summary screen shot.

- An 'original' document is the document chosen to be the representing document from a duplicate set of documents.
- A 'container unextractable document' is a document that could not be extracted from a container (e.g., a password protected ZIP archive where no password was provided to extract archive documents).

Future Improvement:
We have an easy performance improvement in the works that will increase WMS Worker processing/extraction performance by another 30-40%.

### Image 1: Processing Summary
Screen shot of the collection's post-processing report. 
Note: An 'original' document is the document chosen to be the representing document from a duplicate set of documents.

![CorporaProcessingReport](https://github.com/dotfurther/Open-Discover-WhitePaper-2/assets/52750989/d9107d4c-4a30-4ef2-a4c7-4d33d8c5a452)






