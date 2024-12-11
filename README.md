# Tcl String Comparison Bug

This repository demonstrates a common, yet subtle, error in Tcl when comparing strings for equality.  The `badproc` procedure in `bug.tcl` shows an incorrect approach. The corrected version is in `bugSolution.tcl`.

**Bug:** The `badproc` procedure uses `==` to compare strings. However, in Tcl, `==` is a numerical comparison. Thus, it will only return true if the strings represent the same number. This comparison is often unintended and can lead to unpredictable results.

**Solution:** The correct comparison method is to use `eq`, which performs string comparison.

**How to Run:**
1. Save the code snippets in `bug.tcl` and `bugSolution.tcl`. 
2. Run the scripts using a Tcl interpreter (e.g., `tclsh`). 
3. Observe the differing outputs.