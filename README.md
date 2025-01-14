# Haskell Lazy Evaluation Bug
This repository demonstrates a subtle bug in Haskell code that arises from lazy evaluation. The `calculate` function calculates the sum and length of a list. When given an infinite list, the program enters an infinite loop because `length` is never evaluated.

## Bug Description
The bug lies in the `calculate` function.  Due to Haskell's lazy evaluation, the `length` function is only evaluated when its result is needed.  However, in the case of an infinite list, the `sum` function never terminates, so `length` is never called, resulting in an infinite loop.

## Solution
The solution involves forcing the evaluation of the `length` function before calculating the sum. This is achieved by using the `length` function explicitly before calculating the sum.  We also add error handling for infinite lists.

## How to Run
1.  Clone this repository.
2.  Ensure you have the Haskell Platform installed.
3.  Compile and run the files using `ghc` and then executing the compiled binaries.