**GTDI** is a geometric time delay interferometry combination library.

### Introduction to Geometric TDI

Geometric Time Delay Interferometry (Geometric TDI) is a post-processing technique used in space-based gravitational wave detectors (e.g., LISA, Tianqin and Taiji) to suppress laser noises. Its core idea involves constructing a virtual equal-arm interferometer by applying time delays and linear combinations to phase measurement data from detector links, thereby suppressing laser noise.

### Library Overview

The library covers TDI combinations for 8-30 links, and the data files are stored in the folder `data` in the `.txt` format. The file naming convention is `a-b-c(-d).txt`, with the specific meanings as follows:

- `a`: represents the number of links;
- `b`: represents the generation of the TDI combination:
  - `m1g`: modified first-generation TDI combination;
  - `2g`: second-generation TDI combination;
  - `m2g`: modified second-generation TDI combination;
  - `3g`: third-generation TDI combination;
  - `m3g`: modified third-generation TDI combination;
- `c`: TDI, serving as the identifier for the TDI combination;
- `d`: `SF`, representing the sensitivity function. This dataset is the result of deduplication based on the sensitivity function within `a-b-c.txt`.

The combinations in the library are recorded as laser trajectory strings, such as `1<2<1<3>2>3<1<2<1>3<2>1>2>1>2<3>1`, where:

- Numbers represent spacecraft indices;
- `<` and `>` indicate the direction of the virtual laser path in time (forward or backward).

### Mathematica Functions

The combination library file `functions_GTDI.nb` contains relevant functions and examples, which need to be opened with Mathematica. The provided functionalities include:

- Reading geometric TDI combination information;
- Transforming the path of geometric TDI combinations;
- Converting the format of geometric TDI combinations;
- Plotting the spacetime diagram of geometric TDI;
- Calculating and plotting the sensitivity function of TDI combinations;
- Finding equivalent TDI combinations.
