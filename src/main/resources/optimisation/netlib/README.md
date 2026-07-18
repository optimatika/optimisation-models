# NETLIB

The classic NETLIB LP test set, the de facto standard benchmark for
linear programming solvers since the mid-1980s. The collection
contains real-world LP problems from diverse sources (airline
scheduling, forestry, refinery operations, structural optimisation,
etc.) in SIF format. 97 instances included with at most 10k rows and
10k columns. 17 larger instances are listed in the table but not
included.

## References

- D. M. Gay, "Electronic mail distribution of linear programming
  test problems," Mathematical Programming Society COAL Newsletter,
  No. 13, pp. 10-12, 1985.
- T. Koch, "The final NETLIB-LP results," Operations Research Letters,
  32(2), pp. 138-142, 2004.

## Source

| | |
|---|---|
| Downloaded From | numerical.rl.ac.uk/cute/netlib.html |
| Also Available At | netlib.org/lp/data |
| Total Instances | 114 |
| Included | 97 |
| Excluded | 17 |

## Models

Instances marked with `-` in the Incl column exceed the 10k size limit
and are not included here.

| Name | Rows | Cols | Nonzeros | Incl |
|------|-----:|-----:|---------:|:----:|
| 25FV47 | 822 | 1,571 | 5,948 | x |
| 80BAU3B | 2,263 | 9,799 | 17,480 | x |
| ADLITTLE | 57 | 97 | 254 | x |
| AFIRO | 28 | 32 | 46 | x |
| AGG | 489 | 163 | 1,336 | x |
| AGG2 | 517 | 302 | 2,339 | x |
| AGG3 | 517 | 302 | 2,345 | x |
| BANDM | 306 | 472 | 1,487 | x |
| BEACONFD | 174 | 262 | 1,800 | x |
| BLEND | 75 | 83 | 275 | x |
| BNL1 | 644 | 1,175 | 3,328 | x |
| BNL2 | 2,325 | 3,489 | 8,947 | x |
| BOEING1 | 352 | 384 | 1,997 | x |
| BOEING2 | 167 | 143 | 708 | x |
| BORE3D | 234 | 315 | 821 | x |
| BRANDY | 221 | 249 | 1,135 | x |
| CAPRI | 272 | 353 | 952 | x |
| CRE-A | 3,517 | 4,067 | 10,802 | x |
| CRE-B | 9,649 | 72,447 | 178,428 | - |
| CRE-C | 3,069 | 3,678 | 9,719 | x |
| CRE-D | 8,927 | 69,980 | 169,468 | - |
| CYCLE | 1,904 | 2,857 | 11,467 | x |
| CZPROB | 930 | 3,523 | 7,167 | x |
| D2Q06C | 2,172 | 5,167 | 19,169 | x |
| D6CUBE | 416 | 6,184 | 23,470 | x |
| DEGEN2 | 445 | 534 | 2,366 | x |
| DEGEN3 | 1,504 | 1,818 | 13,562 | x |
| DFL001 | 6,072 | 12,230 | 23,000 | - |
| E226 | 224 | 282 | 1,454 | x |
| ETAMACRO | 401 | 688 | 1,403 | x |
| FFFFF800 | 525 | 854 | 3,213 | x |
| FINNIS | 498 | 614 | 1,496 | x |
| FIT1D | 25 | 1,026 | 7,466 | x |
| FIT1P | 628 | 1,677 | 5,768 | x |
| FIT2D | 26 | 10,500 | 71,600 | - |
| FIT2P | 3,001 | 13,525 | 31,897 | - |
| FORPLAN | 71 | 83 | 2,549 | x |
| GANGES | 1,310 | 1,681 | 3,619 | x |
| GFRD-PNC | 617 | 1,092 | 2,182 | x |
| GREENBEA | 2,393 | 5,405 | 16,384 | x |
| GREENBEB | 2,393 | 5,405 | 16,384 | x |
| GROW15 | 301 | 645 | 2,940 | x |
| GROW22 | 441 | 946 | 4,312 | x |
| GROW7 | 141 | 301 | 1,372 | x |
| ISRAEL | 175 | 142 | 1,224 | x |
| KB2 | 44 | 41 | 160 | x |
| KEN-07 | 2,427 | 3,602 | 7,179 | x |
| KEN-11 | 14,695 | 21,349 | 42,645 | - |
| KEN-13 | 28,633 | 42,659 | 85,247 | - |
| KEN-18 | 105,128 | 154,699 | 309,247 | - |
| LOTFI | 154 | 308 | 602 | x |
| MAROS | 847 | 1,443 | 5,335 | x |
| MAROS-R7 | 3,137 | 9,408 | 75,599 | x |
| MODSZK1 | 688 | 1,620 | 2,270 | x |
| NESM | 663 | 2,923 | 7,297 | x |
| OSA-07 | 1,119 | 23,949 | 95,796 | - |
| OSA-14 | 2,338 | 52,460 | 209,840 | - |
| OSA-30 | 4,351 | 100,024 | 400,092 | - |
| OSA-60 | 10,281 | 232,966 | 931,862 | - |
| PDS-02 | 2,954 | 7,535 | 12,716 | x |
| PDS-06 | 9,882 | 28,655 | 49,555 | - |
| PDS-10 | 16,559 | 48,763 | 84,425 | - |
| PDS-20 | 33,875 | 105,728 | 183,916 | - |
| PEROLD | 626 | 1,376 | 3,316 | x |
| PILOT | 1,442 | 3,652 | 22,149 | x |
| PILOT-JA | 941 | 1,988 | 7,828 | x |
| PILOT-WE | 723 | 2,789 | 5,627 | x |
| PILOT4 | 411 | 1,000 | 2,773 | x |
| PILOT87 | 2,031 | 4,883 | 37,685 | x |
| PILOTNOV | 976 | 2,172 | 7,144 | x |
| QAP12 | 3,193 | 8,856 | 47,016 | x |
| QAP15 | 6,331 | 22,275 | 117,000 | - |
| QAP8 | 913 | 1,632 | 8,864 | x |
| RECIPELP | 92 | 180 | 421 | x |
| SC105 | 106 | 103 | 175 | x |
| SC205 | 206 | 203 | 347 | x |
| SC50A | 51 | 48 | 80 | x |
| SC50B | 51 | 48 | 68 | x |
| SCAGR25 | 472 | 500 | 1,065 | x |
| SCAGR7 | 130 | 140 | 291 | x |
| SCFXM1 | 331 | 457 | 1,427 | x |
| SCFXM2 | 661 | 914 | 2,859 | x |
| SCFXM3 | 991 | 1,371 | 4,291 | x |
| SCORPION | 389 | 358 | 941 | x |
| SCRS8 | 491 | 1,169 | 2,182 | x |
| SCSD1 | 78 | 760 | 1,932 | x |
| SCSD6 | 148 | 1,350 | 3,492 | x |
| SCSD8 | 398 | 2,750 | 7,032 | x |
| SCTAP1 | 301 | 480 | 1,236 | x |
| SCTAP2 | 1,091 | 1,880 | 4,928 | x |
| SCTAP3 | 1,481 | 2,480 | 6,518 | x |
| SEBA | 516 | 1,028 | 2,638 | x |
| SHARE1B | 118 | 225 | 624 | x |
| SHARE2B | 97 | 79 | 381 | x |
| SHELL | 537 | 1,775 | 3,119 | x |
| SHIP04L | 403 | 2,118 | 4,232 | x |
| SHIP04S | 403 | 1,458 | 2,912 | x |
| SHIP08L | 779 | 4,283 | 8,556 | x |
| SHIP08S | 779 | 2,387 | 4,764 | x |
| SHIP12L | 1,152 | 5,427 | 10,812 | x |
| SHIP12S | 1,152 | 2,763 | 5,484 | x |
| SIERRA | 1,228 | 2,036 | 5,316 | x |
| STAIR | 357 | 467 | 2,007 | x |
| STANDATA | 360 | 1,075 | 1,827 | x |
| STANDGUB | 362 | 1,184 | 1,936 | x |
| STANDMPS | 468 | 1,075 | 2,043 | x |
| STOCFOR1 | 118 | 111 | 249 | x |
| STOCFOR2 | 2,158 | 2,031 | 5,319 | x |
| STOCFOR3 | 16,676 | 15,695 | 77,756 | - |
| TRUSS | 1,001 | 8,806 | 22,720 | x |
| TUFF | 334 | 587 | 2,398 | x |
| VTP-BASE | 199 | 203 | 523 | x |
| WOOD1P | 245 | 2,594 | 35,284 | x |
| WOODW | 1,099 | 8,405 | 20,487 | x |
