<h1> Unit Testing for python scripts </h1>

__Requirements: Write a set of unit tests to evaluate whether the output is correct using pytest__

Given that unit testing has been established previously using the function pytest, this README will describe how unit testing can be done.

1. Installation:

If you don't have python installed, then you need to install it by asking someone with sudo previledges to perform the following;

``` $ pip install -U pytest ```

Check that installation has been completely correctly by entering the following commands:
  
``` $ pytest -h ```

2. Writing the tests

Create a new test file in the directory and subdirectories (if you have multiple scripts in multiple directories), 
 where the python script is located will make it easier when it comes to running the tests later, though this is not essential.

Save the test files with filenames, such as 
``` test_* ```

or 

```*_test ```

The files must match these patterns for pytest to recognise the files as unit test files.
Alternatively, check that no other files match these patterns.
If there are multiple unit test files present within the project then each must have a unique name

To demonstrate how to write the tests; I will use the reversecomplement.py script as an example.

Navigate to the folder where the reversecomplement.py is stored e.g. ~/Documents/MyFiles/Python/rosalind

In the test file, write the following code:

```import reversecomplement

   def test_reversecomplement():
    input_dna_string = "ACTGACTG"
    output_dna_string = "CAGTCAGT"
    assert reversecomplement_revision.reversecomplement(input_dna_string) == output_dna_string

   def test_reversecomplement_verbose():
    input_dna_string = "ACTGACTG"
    output_text_string = "Here is the reverse complement sequence: 'CAGTCAGT'"
    verbose = True
    assert reversecomplement_revision.reversecomplement(input_dna_string, verbose) == output_text_string
 ```












