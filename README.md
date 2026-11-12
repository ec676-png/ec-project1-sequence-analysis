# ec-project1-sequence-analysis

## Title and Purpose
DNA Mutation Analysis: This project used Python to analyse next-generation sequencing data from six fission yeast samples. It identified DNA mutations and compared mismatch patterns between treated and untreated samples.

## How to Run the Program
The program was written in a Google Colab notebook. First open the Project1_Sequence_Analysis.ipynb in Google Colab, ensure the input files are available, and then run the cells in order.

## Inputs and Outputs
The program used a reference DNA sequence (reference.txt) and a CSV file containing sequencing reads (reads.csv). Each read includes a read ID, sample, group and DNA sequence.
The outputs include identified mutations, their positions and nucleotide substitutions, sample-level summaries, and statistical comparisons between treatment and control groups.

## Code Design
I divided the analysis into five functions so that each stage has a separate purpose. validate_read checks sequence length and valid DNA bases, while find_mutations identifies differences from the reference. analyse_reads combines these functions to process the dataset. I used dictionaries to organise results by sample and count substitutions and mismatch positions. This made it easier to access and update information for individual samples. I also converted sequences to uppercase during validation so that lowercase input would be handled consistently. For the statistical comparison, I calculated mismatch percentages separately for each biological sample rather than treating individual reads as independent replicates. This means the comparison uses the three biological replicates in each group.

## Testing
I tested lowercase sequences, incorrect sequence lengths and invalid DNA characters. I also tested reads with no mutations and an empty dataset. Finally, I ran the complete analysis on the supplied dataset and checked that the sample summaries and statistical comparisons that were produced were correct.
