/*
	********
	*Tests:*
	********
	
command line parameters:
	
	*****************************************************************************************************************************************************************************************************************
	*		Tests			*  		key - 		| 		X - max number  	|       				file name       																								*
	*						*	column number 	|	of records in memory	|		in									       expected out																			*
	*****************************************************************************************************************************************************************************************************************
	* empty file			*		2			|			3				|	tests\test_file_0_in.csv			=>			"Exception occurred: java.io.IOException: empty input file."						*	has 0 records x 0 columns (empty file)	
	* key col has empty val	*		0			|			5				|	tests\test_file_1_in.csv			=>			sorted version by first col															*	has 21 records x 5 columns 	
	* out range key			*		10			|			4				|	tests\test_file_2_in.csv			=>			"Exception occurred: java.lang.ArrayIndexOutOfBoundsException: key out of range."	*	has 10 records x 10 columns
	* out range key			*		-7			|			11				|	tests\test_file_3_in.csv			=>			"Exception occurred: java.lang.ArrayIndexOutOfBoundsException: key out of range."	*	has 10 records x 10 column
	* even n/X,key last col	*		97			|			50				|	tests\test_file_4_in.csv			=>			sorted version by last col															*	has 100 records x 98 columns
	* out range X			*		4			|			-6				|	tests\test_file_5_in.csv			=>			"Exception occurred: java.io.IOException: Given memory range -6 is not valid."		*	has 101 records x 98 columns
	* even X,key 1'st column*		0			|			500				|	tests\test_file_6_in.csv			=>			sorted version by first col															*	has 1000 records x 2 columns
	* X > #records			*		7			|			2000			|	tests\test_file_7_in.csv			=>			sorted version by 7 col																*	has 1001 records x 40 columns
	* valid input, big file	*		19			|			200				|	tests\test_file_8_in.csv			=>			sorted version by 19 col															*	has 50,000 records x 78 columns
	* valid input, big file	*		2			|			3				|	tests\test_file_9_in.csv			=>			sorted version by 2 col																*	has 4 records x 5 columns
	*****************************************************************************************************************************************************************************************************************

