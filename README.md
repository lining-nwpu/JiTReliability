# JiTReliability
This is dataset for JiTReliability.

-----
History
- v1.00 First published[March 2020]
- v1.01 Correct some SZZ errors[May 2021]


-----
Description

This dataset includes 18 open source projects:

1. ActiveMQ
2. Ant
3. Camel
4. Derby
5. Geronimo
6. Hadoop
7. HBase
8. IVY
9. JCR
10. JMeter
11. LOG4J2
12. LUCENE
13. Mahout
14. OpenJPA
15. Pig
16. POI
17. VELOCITY
18. XERCESC

For each project, there are five csv files：  
- **_commitsID.csv  
- **_failures.csv  
- **_input.csv  
- **_input_EB.csv  
- **_mapping.csv  	


1. [PROJECT_NAME]_input.csv:  Software changes, column "bug" indicates if a software change contains software defects. Each column represents:
    - transactionid: an index of each column
    - commitdate: the date when a software change is committed  
    - ns: The number of subsystems modified by a change
    - nm: The number of subdirectories modified by the change
    - nf: The number of files modified by the change
    - entropy: Distribution across the modified files
    - la: Lines of code added
    - ld: Lines of code deleted
    - lt: Lines of code in total
    - fix: whether a changes is a fix
    - ndev: Number of developers
    - pd: Average time gap to the last change over files
    - npt: Number of unique last changes to the files
    - exp: Developer experience, i.e. number of changes
    - rexp: Recent developer experience, i.e. weighted by ages
    - sexp: Developer experience over a subsystem
    - bug: whether a change contains software defects
    - data: commit date presented in number

2. [PROJECT_NAME]_input_EB.csv:
	Software changes, column "bug" indicates if a software change contains early exposed defects.
	
3. [PROJECT_NAME]_failures.csv: Software failures, each column represents:
    - issue.names: The name of a software defect
    - create.date: The date when a defect as reported

4. [PROJECT_NAME]_commitsID.csv: Software changes index, each column represents
    - commit: Software change identifier
    - transactionid: The index of a software change

5. [PROJECT_NAME]_mapping.csv: Software change-defect mapping, each column represents
    - fix: The identifier of the software change which fixed a software defect
    - intro.: The identifier of the software change which introduced a software defect
    - issue: The name of a software change

		
