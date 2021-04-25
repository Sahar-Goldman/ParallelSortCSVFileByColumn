# Parallel sort CSV file by column

## This small project mimic the Filter option of Excel + controls max number of records existing in memory during the run using threads to accelerate merge process.

_Inputs_: **key** - column to be sorted by, the column number.
        **max records in memory** - Number of records program can save at the same time in memory.
        **full file name** - file in CSV format, path included
        
_Output_: **sorted new file** according to given key parameter in new directory - "SortFile\Sorted.csv"
<img src="https://github.com/Sahar-Goldman/ParallelSortCSVFileByColumn/blob/main/csv_sort_exp.PNG">
