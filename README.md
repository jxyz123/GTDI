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

There are 62 data files in the combination library, with the specific information as follows:

| No.  |      filename       | links | generation | number of<br />combinations | delete duplicates<br />based on<br />sensitivity |
| :--: | :-----------------: | :---: | :--------: | :-------------------------: | :----------------------------------------------: |
|  1   |    8-m1g-TDI.txt    |   8   |    1.5     |              4              |                        ×                         |
|  2   |  8-m1g-TDI-SF.txt   |   8   |    1.5     |              3              |                        √                         |
|  3   |   10-m1g-TDI.txt    |  10   |    1.5     |              2              |                        ×                         |
|  4   |   12-m1g-TDI.txt    |  12   |    1.5     |              2              |                        √                         |
|  5   |  12-m1g-TDI-SF.txt  |  12   |    1.5     |             34              |                        ×                         |
|  6   |  12-2g-TDI-SF.txt   |  12   |     2      |             15              |                        √                         |
|  7   |    12-2g-TDI.txt    |  12   |     2      |              3              |                        ×                         |
|  8   |  12-2g-TDI-SF.txt   |  12   |     2      |              2              |                        √                         |
|  9   |   14-m1g-TDI.txt    |  14   |    1.5     |             153             |                        ×                         |
|  10  |  14-m1g-TDI-SF.txt  |  14   |    1.5     |             55              |                        √                         |
|  11  |    14-2g-TDI.txt    |  14   |     2      |              4              |                        ×                         |
|  12  |  14-2g-TDI-SF.txt   |  14   |     2      |              2              |                        √                         |
|  13  |   16-m1g-TDI.txt    |  16   |    1.5     |            1065             |                        ×                         |
|  14  |  16-m1g-TDI-SF.txt  |  16   |    1.5     |             282             |                        √                         |
|  15  |    16-2g-TDI.txt    |  16   |     2      |             38              |                        ×                         |
|  16  |  16-2g-TDI-SF.txt   |  16   |     2      |             11              |                        √                         |
|  17  |   16-m2g-TDI.txt    |  16   |    2.5     |              9              |                        ×                         |
|  18  |  16-m2g-TDI-SF.txt  |  16   |    2.5     |              3              |                        √                         |
|  19  |   18-m1g-TDI.txt    |  18   |    1.5     |            6487             |                        ×                         |
|  20  |  18-m1g-TDI-SF.txt  |  18   |    1.5     |            1093             |                        √                         |
|  21  |    18-2g-TDI.txt    |  18   |     2      |             148             |                        ×                         |
|  22  |  18-2g-TDI-SF.txt   |  18   |     2      |             21              |                        √                         |
|  23  |   18-m2g-TDI.txt    |  18   |    2.5     |             34              |                        ×                         |
|  24  |  18-m2g-TDI-SF.txt  |  18   |    2.5     |              3              |                        √                         |
|  25  |   20-m1g-TDI.txt    |  20   |    1.5     |            44873            |                        ×                         |
|  26  | 20-m1g-TDI-SF-1.txt |  20   |    1.5     |            4655             |                        √                         |
|  27  |    20-2g-TDI.txt    |  20   |     2      |            1000             |                        ×                         |
|  28  |  20-2g-TDI-SF.txt   |  20   |     2      |             114             |                        √                         |
|  29  |   20-m2g-TDI.txt    |  22   |    2.5     |             185             |                        ×                         |
|  30  |  20-m2g-TDI-SF.txt  |  22   |    2.5     |              7              |                        √                         |
|  31  |   22-m1g-TDI.txt    |  22   |    1.5     |           307012            |                        ×                         |
|  32  |  22-m1g-TDI-SF.txt  |  22   |    1.5     |            16718            |                        √                         |
|  33  |    22-2g-TDI.txt    |  22   |     2      |            5559             |                        ×                         |
|  34  |  22-2g-TDI-SF.txt   |  22   |     2      |             383             |                        √                         |
|  35  |   22-m2g-TDI.txt    |  22   |    2.5     |             953             |                        ×                         |
|  36  |  22-m2g-TDI-SF.txt  |  22   |    2.5     |             34              |                        √                         |
|  37  |    24-2g-TDI.txt    |  24   |     2      |            35809            |                        ×                         |
|  38  |  24-2g-TDI-SF.txt   |  24   |     2      |            1591             |                        √                         |
|  39  |   24-m2g-TDI.txt    |  24   |    2.5     |            5868             |                        ×                         |
|  40  |  24-m2g-TDI-SF.txt  |  24   |    2.5     |             163             |                        √                         |
|  41  |    24-3g-TDI.txt    |  24   |     3      |             94              |                        ×                         |
|  42  |  24-3g-TDI-SF.txt   |  24   |     3      |              5              |                        √                         |
|  43  |    26-2g-TDI.txt    |  26   |     2      |           225216            |                        ×                         |
|  44  |  26-2g-TDI-SF.txt   |  26   |     2      |            5378             |                        √                         |
|  45  |   26-m2g-TDI.txt    |  26   |    2.5     |            34942            |                        ×                         |
|  46  |  26-m2g-TDI-SF.txt  |  26   |    2.5     |             547             |                        √                         |
|  47  |    26-3g-TDI.txt    |  26   |     3      |             372             |                        ×                         |
|  48  |  26-3g-TDI-SF.txt   |  26   |     3      |              3              |                        √                         |
|  49  |    28-2g-TDI.txt    |  28   |     2      |           1472444           |                        ×                         |
|  50  | 28-2g-TDI-SF-1.txt  |  28   |     2      |            19055            |                        √                         |
|  51  |   28-m2g-TDI.txt    |  28   |    2.5     |           220177            |                        ×                         |
|  52  |  28-m2g-TDI-SF.txt  |  28   |    2.5     |            2080             |                        √                         |
|  53  |    28-3g-TDI.txt    |  28   |     3      |            2887             |                        ×                         |
|  54  |  28-3g-TDI-SF.txt   |  28   |     3      |             16              |                        √                         |
|  55  |   28-m3g-TDI.txt    |  28   |    3.5     |             45              |                        ×                         |
|  56  |  28-m3g-TDI-SF.txt  |  28   |    3.5     |              3              |                        √                         |
|  57  |   30-m2g-TDI.txt    |  30   |    2.5     |           1388693           |                        ×                         |
|  58  |  30-m2g-TDI-SF.txt  |  30   |    2.5     |            7546             |                        √                         |
|  59  |    30-3g-TDI.txt    |  30   |     3      |            17231            |                        ×                         |
|  60  |  30-3g-TDI-SF.txt   |  30   |     3      |             23              |                        √                         |
|  61  |   30-m3g-TDI.txt    |  30   |    3.5     |             452             |                        ×                         |
|  62  |  30-m3g-TDI-SF.txt  |  30   |    3.5     |              3              |                        √                         |

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
