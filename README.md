# parallel-study-data
Data from player playing the game Parallel, to evaluate player modeling systems


## Data: 
Data from the 3-X group was collected before them taking the lecture on parallel concepts, and 5-X was collected after.

## Files: 

- File Format Specification.pdf:
This file contains general information about the file format of the files inside of the "data" folder.

- annotations.xlsx:
This file contains a full dataset for player modeling (including ground truth), resulting from processing the provided logs.  Each row in the EXCEL file is a time window, and contains a collection of features we calculated (e.g., "number of times they clicked submit", etc.). Those are calculated from the logs, and are the ones we use in our papers.
The last column is what researchers hand annotated as single-thread / multi-thread / trial-error problem solving: 
A: Trial & Error
B: Single Threaded
C: Multi Threaded

- slices.tsv:
This file contains just the ground truth annotations of the data (this is a subset of the information in annotations.xlsx). Each row contains a player ID, a level, a time window and the problem solving strategy (A, B, C) that researchers hand annotated for that time interval.

The “log" folder contains the actual logs (one per session) where each line is an in-game event (such as a mouse click). When players "test" or "submit" a level, SubmitCurrentLevelPlay and TriggerLoadLevel events will occur in the log. The corresponding outcome of testing/submitting can be found in the "data" folder.

The "data" folder contains one file for each time someone clicked on "test" or "submit" and contains the output of the ME (these files are referred to from the files in "log" in SubmitCurrentLevelPlay / TriggerLoadLevel events).

If you use this data set, please use the following citation:

```
@misc{zhu2020understanding,
    title={Understanding Learners' Problem-Solving Strategies in Concurrent and Parallel Programming: A Game-Based Approach},
    author={Jichen Zhu and Katelyn Alderfer and Brian Smith and Bruce Char and Santiago Onta\~{n}\'{o}n},
    year={2020},
    eprint={2005.04789},
    archivePrefix={arXiv},
    primaryClass={cs.HC}
}
```
