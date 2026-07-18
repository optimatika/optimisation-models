# Maros-Meszaros

The Maros-Meszaros convex QP test set in SIF format. All problems have
the form: min c0 + c'x + 1/2 x'Qx, subject to Ax = b, l <= x <= u,
where Q is symmetric positive semidefinite. 113 instances included with
at most 10k rows and 10k columns. 25 larger instances are listed in the
table but not included; they can be downloaded from the original archive.

## References

- I. Maros and Cs. Meszaros, "A Repository of Convex Quadratic
  Programming Problems," Optimization Methods and Software, 11(1-4),
  pp. 671-681, 1999. DOI: 10.1080/10556789908805768
- I. Maros and Cs. Meszaros, "A Repository of Convex Quadratic
  Problems," Technical Report DOC 97/6, Department of Computing,
  Imperial College, London, 1997.

## Source

| | |
|---|---|
| Downloaded From | ftp.numerical.rl.ac.uk/pub/cuter/marosmeszaros |
| Also Available At | github.com/optimizers/maros-meszaros-mirror |
| Total Instances | 138 |
| Included | 113 |
| Excluded | 25 |

## Models

Instances marked with `-` in the Incl column exceed the 10k size limit
and are not included here.

| Name | Vars | Rows | Nonzeros | Q-Nonzeros | Incl |
|------|-----:|-----:|---------:|-----------:|:----:|
| AUG2D | 10,000 | 20,200 | 40,000 | 0 | - |
| AUG2DC | 10,000 | 20,200 | 40,000 | 0 | - |
| AUG2DCQP | 10,000 | 20,200 | 40,000 | 0 | - |
| AUG2DQP | 10,000 | 20,200 | 40,000 | 0 | - |
| AUG3D | 1,000 | 3,873 | 6,546 | 0 | x |
| AUG3DC | 1,000 | 3,873 | 6,546 | 0 | x |
| AUG3DCQP | 1,000 | 3,873 | 6,546 | 0 | x |
| AUG3DQP | 1,000 | 3,873 | 6,546 | 0 | x |
| BOYD1 | 18 | 93,261 | 558,985 | 0 | - |
| BOYD2 | 186,531 | 93,263 | 423,784 | 0 | - |
| CONT-050 | 2,401 | 2,597 | 12,005 | 0 | x |
| CONT-100 | 9,801 | 10,197 | 49,005 | 0 | - |
| CONT-101 | 10,098 | 10,197 | 49,599 | 0 | - |
| CONT-200 | 39,601 | 40,397 | 198,005 | 0 | - |
| CONT-201 | 40,198 | 40,397 | 199,199 | 0 | - |
| CONT-300 | 90,298 | 90,597 | 448,799 | 0 | - |
| CVXQP1L | 5,000 | 10,000 | 14,998 | 29,984 | x |
| CVXQP1M | 500 | 1,000 | 1,498 | 2,984 | x |
| CVXQP1S | 50 | 100 | 148 | 286 | x |
| CVXQP2L | 2,500 | 10,000 | 7,499 | 29,984 | x |
| CVXQP2M | 250 | 1,000 | 749 | 2,984 | x |
| CVXQP2S | 25 | 100 | 74 | 286 | x |
| CVXQP3L | 7,500 | 10,000 | 22,497 | 29,984 | x |
| CVXQP3M | 750 | 1,000 | 2,247 | 2,984 | x |
| CVXQP3S | 75 | 100 | 222 | 286 | x |
| DPKLO1 | 77 | 133 | 1,575 | 0 | x |
| DTOC3 | 9,998 | 14,999 | 34,993 | 0 | - |
| DUAL1 | 1 | 85 | 85 | 3,473 | x |
| DUAL2 | 1 | 96 | 96 | 4,412 | x |
| DUAL3 | 1 | 111 | 111 | 5,997 | x |
| DUAL4 | 1 | 75 | 75 | 2,724 | x |
| DUALC1 | 215 | 9 | 1,935 | 36 | x |
| DUALC2 | 229 | 7 | 1,603 | 21 | x |
| DUALC5 | 278 | 8 | 2,224 | 28 | x |
| DUALC8 | 503 | 8 | 4,024 | 28 | x |
| EXDATA | 3,001 | 3,000 | 7,500 | 1,124,250 | x |
| GENHS28 | 8 | 10 | 24 | 9 | x |
| GOULDQP2 | 349 | 699 | 1,047 | 348 | x |
| GOULDQP3 | 349 | 699 | 1,047 | 697 | x |
| HS118 | 17 | 15 | 39 | 0 | x |
| HS21 | 1 | 2 | 2 | 0 | x |
| HS268 | 5 | 5 | 25 | 10 | x |
| HS35 | 1 | 3 | 3 | 2 | x |
| HS35MOD | 1 | 3 | 3 | 2 | x |
| HS51 | 3 | 5 | 7 | 2 | x |
| HS52 | 3 | 5 | 7 | 2 | x |
| HS53 | 3 | 5 | 7 | 2 | x |
| HS76 | 3 | 4 | 10 | 2 | x |
| HUES-MOD | 2 | 10,000 | 19,899 | 0 | x |
| HUESTIS | 2 | 10,000 | 19,899 | 0 | x |
| KSIP | 1,001 | 20 | 18,411 | 0 | x |
| LASER | 1,000 | 1,002 | 3,000 | 3,000 | x |
| LISWET1 | 10,000 | 10,002 | 30,000 | 0 | - |
| LISWET10 | 10,000 | 10,002 | 30,000 | 0 | - |
| LISWET11 | 10,000 | 10,002 | 30,000 | 0 | - |
| LISWET12 | 10,000 | 10,002 | 30,000 | 0 | - |
| LISWET2 | 10,000 | 10,002 | 30,000 | 0 | - |
| LISWET3 | 10,000 | 10,002 | 30,000 | 0 | - |
| LISWET4 | 10,000 | 10,002 | 30,000 | 0 | - |
| LISWET5 | 10,000 | 10,002 | 30,000 | 0 | - |
| LISWET6 | 10,000 | 10,002 | 30,000 | 0 | - |
| LISWET7 | 10,000 | 10,002 | 30,000 | 0 | - |
| LISWET8 | 10,000 | 10,002 | 30,000 | 0 | - |
| LISWET9 | 10,000 | 10,002 | 30,000 | 0 | - |
| LOTSCHD | 7 | 12 | 54 | 0 | x |
| MOSARQP1 | 700 | 2,500 | 3,422 | 45 | x |
| MOSARQP2 | 600 | 900 | 2,930 | 45 | x |
| POWELL20 | 10,000 | 10,000 | 20,000 | 0 | x |
| PRIMAL1 | 85 | 325 | 5,815 | 0 | x |
| PRIMAL2 | 96 | 649 | 8,042 | 0 | x |
| PRIMAL3 | 111 | 745 | 21,547 | 0 | x |
| PRIMAL4 | 75 | 1,489 | 16,031 | 0 | x |
| PRIMALC1 | 9 | 230 | 2,070 | 0 | x |
| PRIMALC2 | 7 | 231 | 1,617 | 0 | x |
| PRIMALC5 | 8 | 287 | 2,296 | 0 | x |
| PRIMALC8 | 8 | 520 | 4,160 | 0 | x |
| Q25FV47 | 820 | 1,571 | 10,400 | 59,053 | x |
| QADLITTL | 56 | 97 | 383 | 70 | x |
| QAFIRO | 27 | 32 | 83 | 3 | x |
| QBANDM | 305 | 472 | 2,494 | 16 | x |
| QBEACONF | 173 | 262 | 3,375 | 9 | x |
| QBORE3D | 233 | 315 | 1,429 | 50 | x |
| QBRANDY | 220 | 249 | 2,148 | 49 | x |
| QCAPRI | 271 | 353 | 1,767 | 838 | x |
| QE226 | 223 | 282 | 2,578 | 897 | x |
| QETAMACR | 400 | 688 | 2,409 | 4,069 | x |
| QFFFFF80 | 524 | 854 | 6,227 | 1,638 | x |
| QFORPLAN | 161 | 421 | 4,563 | 546 | x |
| QGFRDXPN | 616 | 1,092 | 2,377 | 108 | x |
| QGROW15 | 300 | 645 | 5,620 | 462 | x |
| QGROW22 | 440 | 946 | 8,252 | 787 | x |
| QGROW7 | 140 | 301 | 2,612 | 327 | x |
| QISRAEL | 174 | 142 | 2,269 | 656 | x |
| QPCBLEND | 74 | 83 | 491 | 0 | x |
| QPCBOEI1 | 351 | 384 | 3,485 | 0 | x |
| QPCBOEI2 | 166 | 143 | 1,196 | 0 | x |
| QPCSTAIR | 356 | 467 | 3,856 | 0 | x |
| QPILOTNO | 975 | 2,172 | 13,057 | 391 | x |
| QPTEST | 2 | 2 | 4 | 1 | x |
| QRECIPE | 91 | 180 | 663 | 30 | x |
| QSC205 | 205 | 203 | 551 | 10 | x |
| QSCAGR25 | 471 | 500 | 1,554 | 100 | x |
| QSCAGR7 | 129 | 140 | 420 | 17 | x |
| QSCFXM1 | 330 | 457 | 2,589 | 677 | x |
| QSCFXM2 | 660 | 914 | 5,183 | 1,057 | x |
| QSCFXM3 | 990 | 1,371 | 7,777 | 1,132 | x |
| QSCORPIO | 388 | 358 | 1,426 | 18 | x |
| QSCRS8 | 490 | 1,169 | 3,182 | 88 | x |
| QSCSD1 | 77 | 760 | 2,388 | 691 | x |
| QSCSD6 | 147 | 1,350 | 4,316 | 1,308 | x |
| QSCSD8 | 397 | 2,750 | 8,584 | 2,370 | x |
| QSCTAP1 | 300 | 480 | 1,692 | 117 | x |
| QSCTAP2 | 1,090 | 1,880 | 6,714 | 636 | x |
| QSCTAP3 | 1,480 | 2,480 | 8,874 | 861 | x |
| QSEBA | 515 | 1,028 | 4,352 | 550 | x |
| QSHARE1B | 117 | 225 | 1,151 | 21 | x |
| QSHARE2B | 96 | 79 | 694 | 45 | x |
| QSHELL | 536 | 1,775 | 3,556 | 34,385 | x |
| QSHIP04L | 402 | 2,118 | 6,332 | 42 | x |
| QSHIP04S | 402 | 1,458 | 4,352 | 42 | x |
| QSHIP08L | 778 | 4,283 | 12,802 | 34,025 | x |
| QSHIP08S | 778 | 2,387 | 7,114 | 11,139 | x |
| QSHIP12L | 1,151 | 5,427 | 16,170 | 60,205 | x |
| QSHIP12S | 1,151 | 2,763 | 8,178 | 16,361 | x |
| QSIERRA | 1,227 | 2,036 | 7,302 | 61 | x |
| QSTAIR | 356 | 467 | 3,856 | 952 | x |
| QSTANDAT | 359 | 1,075 | 3,031 | 666 | x |
| S268 | 5 | 5 | 25 | 10 | x |
| STADAT1 | 3,999 | 2,001 | 9,997 | 0 | x |
| STADAT2 | 3,999 | 2,001 | 9,997 | 0 | x |
| STADAT3 | 7,999 | 4,001 | 19,997 | 0 | x |
| STCQP1 | 2,052 | 4,097 | 13,338 | 22,506 | x |
| STCQP2 | 2,052 | 4,097 | 13,338 | 22,506 | x |
| TAME | 1 | 2 | 2 | 1 | x |
| UBH1 | 12,000 | 18,009 | 48,000 | 0 | - |
| VALUES | 1 | 202 | 202 | 3,620 | x |
| YAO | 2,000 | 2,002 | 6,000 | 0 | x |
| ZECEVIC2 | 2 | 2 | 4 | 0 | x |
