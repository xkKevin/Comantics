# Revealing the Semantics of Data Wrangling Scripts With COMANTICS

This repository contains the supplemental material for "Revealing the Semantics of Data Wrangling Scripts With COMANTICS".

This work contributes COMANTICS to automatically review the semantics of data wrangling scripts.
Given a piece of wrangling code with its source tables, COMANTICS will detect the differences between intermediate input and output tables, and infer the transformation types and their parameters.
Those inference results can be applied to various downstream tasks, such as Code Annotation, Semantics Visualization, and Table Comparison.


## Content

- 1-dataset.xlsx: A real-world dataset including 921 lines of wrangling code where each is annotated with a data transformation.
- 2-transformation-type-results.csv: The unabridged frequency ranking of data transformation types in our dataset. We have provided the number of each transformation type with its percentage in Python, R, and Sum groups, respectively.
- 3-transformation-type-analysis.pdf: The analysis of commonly used transformations.
- 4-functions-with-frequences.csv: The 99 functions (including the None function, i.e., the non-functional equation) with their frequencies in our dataset.
- 5-qualitative-coding&the-design-space.pdf: Detailed descriptions of our qualitative coding method and the construction of our design space for table changes. We also provide a description for each characteristic in the design space.
- 6-mapping-table.xlsx: A mapping between data transformations and characteristics of table changes. The description of each transformation and characteristic is presented in 2-transformation-type-results.csv and 5-qualitative-coding&the-design-space.pdf, respectively.
    > Note that to make full use of the characteristics of table changes to distinguish different transformation types, we have subdivided the transformations *transform_tables_fold* and *transform_tables_unfold* into three cases, respectively. Taking the *transform_tables_fold* as an example, it folds multiple columns into two columns, i.e., the key column and the value column. If the number of columns to be folded is 1, 2, and greater than 2 (>2), which corresponds to *transform_tables_fold(1)*, *transform_tables_fold(2)*, and *transform_tables_fold(>2)*, the number of columns in the table will be increased, unchanged, and decreased, and the number of rows will be unchanged, increased, and increased, respectively. 
- 7-CNN-model.pdf: The structure of the Siamese convolutional neural network model in our pipeline.
- 8-the-completion-time.pdf: An additional quantitative experiment to assess how the completion time of COMANTICS is affected by table sizes.
- 9-all-confusion-matrix.svg: The normalized confusion matrix of the 5th experiment setting. 
- 10-video.mp4: A video that demonstrates the key steps of COMANTICS and its two applications in different scenarios.

## Reference

K. Xiong, Z. Luo, S. Fu, Y. Wang, M. Xu, and Y. Wu. Revealing the Semantics of Data Wrangling Scripts With COMANTICS. *IEEE Transactions on Visualization and Computer Graphics*, 29(1):117–127, 2023. doi: [10.1109/TVCG.2022.3209470](https://doi.org/10.1109/TVCG.2022.3209470)

