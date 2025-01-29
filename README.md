# F# Mutable Variable Swap Bug

This repository demonstrates a common error in F# when dealing with mutable variables. The example showcases unexpected behavior when attempting to swap two mutable variables using a function.

## Bug Description

In F#, mutable variables are passed by reference to functions. When a function modifies a mutable variable, it directly affects the original variable. The provided code attempts to swap two mutable variables, but the result is not as expected because the function modifies the original variables directly rather than using copies.

## Solution

The solution avoids the issues caused by pass-by-reference by using tuples to return the swapped values. This ensures that the original variables remain unchanged within their scope.