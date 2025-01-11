**GTDI** is a geometric time delay interferometry combination library.

The library covers TDI combinations for 8-30 links, and the data files are stored in the folder `data` in the `.wdx` format. The file naming convention is `a-b-c(-d).wdx`, with the specific meanings as follows:
- `a`: represents the number of links;
- `b`: represents the generation of the TDI combination, `m1g` indicates the modified first-generation TDI combination; `2g` indicates the second-generation TDI combination; `m2g` indicates the modified second-generation TDI combination; `3g` indicates the third-generation TDI combination and `m3g` indicates the modified third-generation TDI combination;
- `c`: TDI, serving as the identifier for the TDI combination;
- `d`: `SF`, representing the sensitivity function. This dataset is the result of deduplication based on the sensitivity function within `a-b-c.wdx`. `SF-1` indicates that due to the excessive amount of TDI combination data, the deduplication was not fully carried out according to the sensitivity function.

The combination library file `functions_GTDI.nb` contains relevant functions and examples, which need to be opened with Mathematica. The provided functionalities include:
- Reading geometric TDI combination information;
- Transforming the path of geometric TDI combinations;
- Converting the format of geometric TDI combinations;
- Plotting the spacetime diagram of geometric TDI;
- Calculating and plotting the sensitivity function of TDI combinations.

Note: The WDX (Wolfram Data Exchange) file format is a binary format used by the Wolfram Language for storing and exchanging expressions and data.
