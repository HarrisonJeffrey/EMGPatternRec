# EMGPatternRec
Work for a research project on training machine learning models to classify 17 different hand movements from 11 people with amputations and 11 people without for comparison to indentify if researching on the more readily available non-disabled data can be an acceptable substitute.

## Abstract
Surface electromyography (sEMG) pattern recognition has forged the primary focus on
myoelectric controlled prostheses and yet a great volume of research utilises signal data
solely from intact subjects. This paper will address whether it is suitable to focus entirely
on intact subjects when examining performance in different feature extraction and machine
learning classifiers or if, in fact, it results in misplaced confidence. The experimental results
displayed a discernible pattern where the best performing feature extraction and classifier
combination tended to be the same across both sets of intact and amputee data, with the
same being said for the majority of combinations down to the worst performing. From
these, the highest classification accuracy for the entire datasets occurred in the intact set at
66% with a mean absolute value (MAV) feature extraction and k-nearest neighbor (k-NN)
classifier - dropping by 32% to 45% on the amputee set. It was noted that any improvement
on the intact set was re
ected on the amputee set, or when combining the both, showing
that research on intact subjects can be a suitable substitute when amputee data is difficult
to produce.

## Data and Instructions
The datasets used for this project came from http://ninaweb.hevs.ch/, specifically datasets 2 and 3. All data can be acquired from that website for free once creating an account. The files provided are .mat files and, in order to work within Jupyter Notebook, the EMG, rerepetition, and restimulus columns were extracted as CSV files and saved in either the DB2 or DB3 folder (dependent on which dataset the subjects came from) following the naming convention "DB[dataset number]_S[subject number]_E[exercise number]_#[column name].csv".

With the data successfully stored in the correct directory, simply load the 'preprocessing' notebook and run all cells to unify the subject data, standardise it, then perform windowing and feature extraction (this may take some time). This should populate the 'dataset' directory and subdirectories ready for classifying through the 'classifiers' notebook which requires just running all the cells to run six sets of tests (training on individuals within a dataset or pairing in both, training on each entire dataset/both) for the three feature extraction methods and three classifiers (for a grand total of 54 tests, so this will definitely take quite some time!). At the end of the notebook the results are visualised as bar and scatter charts.

Average classification accuracy when trained on individual subjects:-
[[https://github.com/harrisonjeffrey/EMGPatternRec/blob/master/img/classification_ind.png|alt=classification accuracy]]

[[https://github.com/harrisonjeffrey/EMGPatternRec/blob/master/img/classification_ind_scatter.png|alt=classification accuracy]]
Classification accuracy when trained on entire datasets:-
[[https://github.com/harrisonjeffrey/EMGPatternRec/blob/master/img/classification_whole.png|alt=classification accuracy]]

[[https://github.com/harrisonjeffrey/EMGPatternRec/blob/master/img/classification_whole_scatter.png|alt=classification accuracy]]
