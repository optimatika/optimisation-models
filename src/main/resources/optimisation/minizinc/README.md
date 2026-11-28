# MiniZinc Collection

Models from the [MiniZinc benchmark suite](https://github.com/MiniZinc/minizinc-benchmarks) – mostly constraint programming problems, from the MiniZinc Challenges 2008–2012 and later – compiled to FlatZinc with MiniZinc 2.11.0 and its linear library (`-Glinear`, the one MiniZinc uses for MIP solvers). So every model is a MIP: integer and binary variables with linear constraints. Read them with ojAlgo as `ExpressionsBasedModel.FileFormat.FZN`.

Up to 5 instances per problem, spread over the problem's range of instance sizes, with at least 10 and at most 10k variables, and at most 10k constraints, as ojAlgo reads them. Each file starts with a comment that says which model and data it was compiled from.

The models and data are under the MIT license, see [LICENSE](LICENSE). A few models carry a copyright notice of their own, under similar terms – it is kept at the top of the files made from them.

## Reference results

[MINIZINC.solu](MINIZINC.solu) has a status – and objective value – per model, from HiGHS with a 30 s time limit. "solved" is a solution to a satisfaction problem. "feasible" (a solution, not proven optimal) and "unknown" only mean HiGHS did not get further in that time.

Then checked against the [MiniZinc Challenge](https://www.minizinc.org/challenge/) results, 2010–2026 – each year's per-instance results are at `https://www.minizinc.org/challenge/<year>/results.json`. 185 of the models are challenge instances. Where a challenge solver proved an optimum, that optimum is used – once CP-SAT or SCIP proved, or reached, the same value on the FlatZinc file here, as a challenge instance can be another version of the model. That made 49 more models optimal, and the challenge agrees with all 88 of HiGHS's optimal values that are challenge instances. One, `gfd-schedule__n30f3d30m7k4`, is another version: CP-SAT and HiGHS both prove 8 here, the challenge's optimum is 1 – so it is optimal 8. Eight more have a proven challenge optimum that nothing has reached here yet, so they are still feasible or unknown. HiGHS 1.16 also called `hrc__exp2-1-4795` unsat – it has an optimum, 5. The other unsat ones are proven unsat by CP-SAT too.

| Status | Models |
|:-------|-------:|
| optimal | 251 |
| solved | 91 |
| feasible | 60 |
| unsat | 12 |
| unknown | 35 |

## Categories

One folder per category, by what the problem is about, each with a list of its models (`<category>.dat`). [MINIZINC.dat](MINIZINC.dat) lists all models, as `<category>/<name>`. The solver does not see the category – FlatZinc has no such label.

| Category | Models | Problems |
|:---------|-------:|:---------|
| [assignment-location](assignment-location) | 42 | celar, city-position, depot-placement, fast-food, hrc, mapping, photo, radiation, table-layout |
| [configuration](configuration) | 10 | java-auto-gen, zephyrus |
| [design](design) | 49 | bibd, costas-array, debruijn_binary, ghoulomb, golfers, golomb, langford, p1f, schur_numbers, steiner-triples, still-life-wastage, still_life, still_life2, triangular |
| [graph](graph) | 30 | community-detection, diameterc-mst, grid-colouring, maximum-dag, sugiyama, tc-graph-color |
| [other](other) | 18 | is, jp-encoding, nfc, opt-cryptanalysis, parity-learning, pattern-set-mining |
| [packing-cutting](packing-cutting) | 36 | 2DBinPacking, carpet-cutting, cutstock, freepizza, market_split, multi-knapsack, rectangle-packing, template_design |
| [puzzle](puzzle) | 67 | alpha, amaze, areas, fillomino, kakuro, knights, latin-squares, magicseq, mqueens, nmseq, nonogram, pentominoes, QCP, quasigroup7, queens, solbat, tents |
| [rostering-timetabling](rostering-timetabling) | 32 | bacp, bus_scheduling, curriculum, gbac, league, nsp, on-call-rostering |
| [routing](routing) | 52 | cvrp, java-routing, ma-path-finding, mario, prize-collecting, shortest_path, stochastic-vrp, tpp, traveling-tppv, trucking, trucking_hl, vrp |
| [scheduling](scheduling) | 87 | cargo, cyclic-rcpsp, evilshop, filters, flexible-jobshop, gfd-schedule, jobshop, jobshop2, mrcpsp, openshop, project-planning, rcpsp, rcpsp-max, rcpsp-wet, road-cons, ship-schedule, smelt, spot5, stochastic-fjsp, train |
| [sequencing](sequencing) | 20 | cars, carseq, open_stacks, talent_scheduling |
| [synthetic](synthetic) | 6 | prop_stress, search_stress, search_stress2, slow_convergence |

## Models

| Name | Category | Variables | Integers | Constraints | Goal | Reference |
|:-----|:---------|----------:|---------:|------------:|:-----|:----------|
| 2DBinPacking__class_10_Class10_60_9 | packing-cutting | 3,659 | 3,659 | 3,895 | min | optimal 9 |
| 2DBinPacking__class_1_Class1_20_4 | packing-cutting | 419 | 419 | 495 | min | optimal 6 |
| 2DBinPacking__class_3_Class3_40_5 | packing-cutting | 1,639 | 1,639 | 1,795 | min | optimal 12 |
| 2DBinPacking__class_7_Class7_20_9 | packing-cutting | 419 | 419 | 495 | min | optimal 6 |
| 2DBinPacking__class_9_Class9_40_8 | packing-cutting | 1,639 | 1,639 | 1,795 | min | optimal 26 |
| alpha__alpha | puzzle | 702 | 702 | 98 | sat | solved |
| amaze__2012-03-15 | puzzle | 2,153 | 2,153 | 2,180 | min | optimal 1429 |
| amaze__2012-04-27 | puzzle | 1,375 | 1,375 | 1,206 | min | unknown |
| amaze__2012-07-04 | puzzle | 1,394 | 1,394 | 1,225 | min | optimal 481 |
| amaze__2012-07-27 | puzzle | 1,898 | 1,898 | 1,803 | min | unknown |
| amaze__amaze | puzzle | 295 | 295 | 267 | min | optimal 12 |
| areas__3_3_3 | puzzle | 48 | 48 | 85 | sat | solved |
| areas__5_5_9 | puzzle | 179 | 179 | 262 | sat | solved |
| bacp__bacp-14 | rostering-timetabling | 961 | 961 | 626 | min | optimal 27 |
| bacp__bacp-27 | rostering-timetabling | 961 | 961 | 622 | min | optimal 34 |
| bacp__bacp-28 | rostering-timetabling | 961 | 961 | 614 | min | optimal 28 |
| bacp__bacp-4 | rostering-timetabling | 961 | 961 | 640 | min | optimal 44 |
| bacp__bacp-9 | rostering-timetabling | 961 | 961 | 629 | min | optimal 38 |
| bibd__06_03_02 | design | 418 | 418 | 911 | sat | solved |
| bibd__08_04_03 | design | 908 | 908 | 2,054 | sat | solved |
| bibd__09_03_01 | design | 930 | 930 | 2,152 | sat | solved |
| bibd__16_04_01 | design | 3,928 | 3,928 | 9,806 | sat | unknown |
| bus_scheduling__c1a | rostering-timetabling | 7,544 | 7,544 | 165 | min | unknown |
| bus_scheduling__r1 | rostering-timetabling | 2,504 | 2,504 | 54 | min | optimal 11 |
| bus_scheduling__r5 | rostering-timetabling | 2,203 | 2,203 | 189 | min | optimal 29 |
| bus_scheduling__t1 | rostering-timetabling | 78 | 78 | 23 | min | optimal 7 |
| bus_scheduling__t2 | rostering-timetabling | 3,016 | 3,016 | 107 | min | optimal 19 |
| cargo__challenge01_0s_1913 | scheduling | 4,240 | 4,240 | 6,929 | min | optimal 0 |
| cargo__challenge02_0s_1139 | scheduling | 4,482 | 4,482 | 7,360 | min | optimal 25 |
| cargo__challenge04_1s_626 | scheduling | 4,206 | 4,206 | 6,880 | min | optimal 714 |
| cargo__challenge05_1s_954 | scheduling | 4,646 | 4,646 | 7,686 | min | optimal 2883 |
| cargo__challenge06_1s_3927 | scheduling | 5,902 | 5,902 | 9,800 | min | optimal 3394 |
| carpet-cutting__mzn_rnd_test.01 | packing-cutting | 942 | 942 | 2,046 | min | optimal 621 |
| carpet-cutting__mzn_rnd_test.02 | packing-cutting | 583 | 583 | 1,258 | min | optimal 919 |
| carpet-cutting__mzn_rnd_test.11 | packing-cutting | 768 | 768 | 1,656 | min | optimal 963 |
| carpet-cutting__mzn_rnd_test.13 | packing-cutting | 4,297 | 4,297 | 9,215 | min | feasible 812 |
| carpet-cutting__mzn_rnd_test.16 | packing-cutting | 4,111 | 4,111 | 8,869 | min | feasible 2545 |
| cars__cars1 | sequencing | 110 | 110 | 103 | sat | solved |
| cars__cars_65_03 | sequencing | 6,200 | 6,200 | 2,412 | sat | solved |
| cars__cars_75_04 | sequencing | 5,800 | 5,800 | 2,410 | sat | solved |
| cars__cars_80_01 | sequencing | 6,400 | 6,400 | 2,413 | sat | solved |
| cars__cars_85_03 | sequencing | 7,200 | 7,200 | 2,417 | sat | solved |
| carseq__carseq_set_1_car_40 | sequencing | 6,400 | 6,400 | 3,400 | sat | solved |
| carseq__carseq_set_1_car_57 | sequencing | 6,000 | 6,000 | 3,398 | sat | solved |
| carseq__carseq_set_1_car_6 | sequencing | 2,900 | 2,900 | 1,697 | sat | unknown |
| carseq__carseq_set_1_car_62 | sequencing | 7,200 | 7,200 | 3,404 | sat | solved |
| carseq__test_car_test_1 | sequencing | 66 | 66 | 76 | sat | solved |
| celar__CELAR6-SUB0 | assignment-location | 2,603 | 2,603 | 2,470 | min | optimal 159 |
| celar__CELAR6-SUB2 | assignment-location | 3,575 | 3,575 | 4,076 | min | feasible 6200 |
| celar__CELAR6-SUB3 | assignment-location | 4,169 | 4,169 | 4,848 | min | feasible 13229 |
| celar__CELAR6-SUB4 | assignment-location | 4,829 | 4,829 | 5,512 | min | feasible 24542 |
| celar__CELAR7-SUB3 | assignment-location | 4,169 | 4,169 | 4,848 | min | feasible 5573422 |
| city-position__city-4-04 | assignment-location | 57 | 57 | 94 | min | optimal 31 |
| city-position__city-5-05 | assignment-location | 144 | 144 | 248 | min | optimal 2850 |
| city-position__city-5-06 | assignment-location | 162 | 162 | 282 | min | optimal 3493 |
| city-position__city-7-04 | assignment-location | 258 | 258 | 452 | min | optimal 2930 |
| city-position__city-8-06 | assignment-location | 435 | 435 | 772 | min | feasible 62801 |
| community-detection__dolphin.s124.k4 | graph | 698 | 698 | 1,078 | max | unsat |
| community-detection__mexican.s26.k4 | graph | 1,101 | 1,101 | 1,725 | max | feasible 18 |
| community-detection__Sampson.s10.k3 | graph | 693 | 693 | 1,095 | max | optimal 10 |
| community-detection__Sampson.s20.k4 | graph | 494 | 494 | 756 | max | feasible 4 |
| community-detection__Strike.s2.k8 | graph | 992 | 992 | 1,388 | max | optimal 75 |
| costas-array__15 | design | 3,259 | 3,259 | 804 | sat | unknown |
| costas-array__17 | design | 4,764 | 4,764 | 1,046 | sat | unknown |
| costas-array__20 | design | 7,794 | 7,794 | 1,469 | sat | unknown |
| costas-array__4 | design | 62 | 62 | 44 | sat | solved |
| costas-array__6 | design | 199 | 199 | 111 | sat | solved |
| curriculum__curriculum_10 | rostering-timetabling | 809 | 809 | 512 | min | optimal 14 |
| curriculum__curriculum_12 | rostering-timetabling | 1,531 | 1,531 | 927 | min | optimal 17 |
| curriculum__curriculum_8 | rostering-timetabling | 699 | 699 | 447 | min | optimal 17 |
| cutstock__small_test0 | packing-cutting | 29 | 29 | 11 | min | optimal 4 |
| cutstock__type13_TEST1 | packing-cutting | 870 | 870 | 90 | min | optimal 63 |
| cutstock__type13_TEST5 | packing-cutting | 1,002 | 1,002 | 102 | min | optimal 67 |
| cutstock__type14_TEST6 | packing-cutting | 9,197 | 9,197 | 847 | min | feasible 733 |
| cutstock__type15_TEST7 | packing-cutting | 4,159 | 4,159 | 219 | min | optimal 171 |
| cvrp__simple2 | routing | 867 | 867 | 2,658 | min | optimal 34 |
| cyclic-rcpsp__easy_3 | scheduling | 3,464 | 3,464 | 3,145 | min | optimal 1920 |
| cyclic-rcpsp__hard_6 | scheduling | 2,693 | 2,693 | 2,501 | min | feasible 1433 |
| cyclic-rcpsp__medium_1 | scheduling | 1,143 | 1,143 | 1,219 | min | optimal 585 |
| cyclic-rcpsp__medium_2 | scheduling | 1,013 | 1,013 | 1,100 | min | optimal 516 |
| cyclic-rcpsp__medium_3 | scheduling | 3,977 | 3,977 | 7,911 | min | optimal 3132 |
| debruijn_binary__02_03 | design | 97 | 97 | 57 | sat | solved |
| depot-placement__att48_6 | assignment-location | 3,546 | 3,546 | 495 | min | optimal 13995 |
| depot-placement__rat99_4 | assignment-location | 1,850 | 1,850 | 279 | min | optimal 105 |
| depot-placement__st70_4 | assignment-location | 1,850 | 1,850 | 279 | min | optimal 145 |
| depot-placement__ulysses16_4 | assignment-location | 1,850 | 1,850 | 279 | min | feasible 2886 |
| depot-placement__ulysses22_6 | assignment-location | 3,546 | 3,546 | 495 | min | feasible 5501 |
| diameterc-mst__c_v15_a105_d4 | graph | 1,302 | 1,302 | 3,311 | min | optimal 346 |
| diameterc-mst__c_v20_a190_d5 | graph | 2,780 | 2,780 | 7,573 | min | optimal 414 |
| diameterc-mst__s_v20_a50_d4 | graph | 1,121 | 1,121 | 2,144 | min | optimal 442 |
| diameterc-mst__s_v20_a50_d5 | graph | 1,317 | 1,317 | 2,427 | min | optimal 381 |
| diameterc-mst__s_v40_a100_d5 | graph | 3,888 | 3,888 | 7,375 | min | optimal 729 |
| evilshop__js-brs2-5 | scheduling | 1,006 | 1,006 | 2,206 | min | optimal 77406 |
| evilshop__js-brs2-7 | scheduling | 1,968 | 1,968 | 4,488 | min | feasible 87494 |
| evilshop__js-setg2-10 | scheduling | 2,011 | 2,011 | 4,711 | min | feasible 64311 |
| evilshop__js-setg2-5 | scheduling | 506 | 506 | 1,106 | min | optimal 40837 |
| evilshop__js-setg2-7 | scheduling | 988 | 988 | 2,248 | min | optimal 46075 |
| fast-food__ff3 | assignment-location | 779 | 779 | 1,326 | min | optimal 1330 |
| fast-food__ff32 | assignment-location | 66 | 66 | 108 | min | optimal 5708 |
| fast-food__ff6 | assignment-location | 2,915 | 2,915 | 5,072 | min | optimal 2 |
| fast-food__ff65 | assignment-location | 1,675 | 1,675 | 2,906 | min | optimal 63 |
| fast-food__ff86 | assignment-location | 470 | 470 | 805 | min | optimal 413 |
| fillomino__01 | puzzle | 267 | 267 | 384 | sat | solved |
| fillomino__11 | puzzle | 755 | 755 | 1,302 | sat | solved |
| fillomino__16 | puzzle | 847 | 847 | 1,445 | sat | solved |
| fillomino__20 | puzzle | 892 | 892 | 1,500 | sat | solved |
| fillomino__7x7_0 | puzzle | 2,910 | 2,910 | 5,217 | sat | unknown |
| filters__ar_1_2 | scheduling | 649 | 649 | 819 | min | optimal 18 |
| filters__dct_1_1 | scheduling | 1,241 | 1,241 | 1,857 | min | optimal 34 |
| filters__dct_4_4 | scheduling | 2,473 | 2,473 | 3,041 | min | feasible 11 |
| filters__fir16_1_2 | scheduling | 805 | 805 | 1,028 | min | optimal 19 |
| filters__fir_1_1 | scheduling | 278 | 278 | 404 | min | optimal 18 |
| flexible-jobshop__easy01 | scheduling | 4,673 | 4,673 | 7,098 | min | optimal 253 |
| flexible-jobshop__med10 | scheduling | 1,781 | 1,781 | 3,620 | min | feasible 954 |
| freepizza__pizza6 | packing-cutting | 489 | 489 | 426 | min | optimal 210 |
| gbac__reduced_UD10-gbac | rostering-timetabling | 4,024 | 4,024 | 1,030 | min | optimal 1015 |
| gbac__reduced_UD4-gbac | rostering-timetabling | 4,754 | 4,754 | 1,050 | min | optimal 949 |
| gbac__reduced_UD6-gbac | rostering-timetabling | 2,685 | 2,685 | 930 | min | optimal 225 |
| gbac__toy-gbac | rostering-timetabling | 388 | 388 | 140 | min | optimal 191 |
| gfd-schedule__n10f2d10m10k3 | scheduling | 864 | 864 | 1,018 | min | optimal 3 |
| gfd-schedule__n25f5d20m10k3 | scheduling | 4,116 | 4,116 | 6,430 | min | optimal 5 |
| gfd-schedule__n30f3d30m7k4 | scheduling | 5,843 | 5,843 | 9,015 | min | optimal 8 |
| ghoulomb__3-3-3 | design | 99 | 99 | 57 | min | optimal 3 |
| ghoulomb__3-4-6 | design | 711 | 711 | 136 | min | optimal 6 |
| golfers__golfers_2_2_3 | design | 172 | 172 | 246 | sat | solved |
| golfers__golfers_5_2_8 | design | 4,980 | 4,980 | 8,360 | sat | unknown |
| golomb__03 | design | 33 | 33 | 19 | min | optimal 3 |
| golomb__05 | design | 270 | 270 | 56 | min | optimal 11 |
| golomb__07 | design | 1,071 | 1,071 | 113 | min | optimal 25 |
| golomb__10 | design | 4,590 | 4,590 | 236 | min | unknown |
| golomb__12 | design | 9,636 | 9,636 | 343 | min | unknown |
| grid-colouring__10_5 | graph | 1,676 | 1,676 | 2,450 | min | optimal 3 |
| grid-colouring__4_11 | graph | 1,475 | 1,475 | 2,090 | min | optimal 3 |
| grid-colouring__4_8 | graph | 833 | 833 | 1,160 | min | optimal 3 |
| grid-colouring__5_6 | graph | 706 | 706 | 990 | min | optimal 3 |
| grid-colouring__7_8 | graph | 1,877 | 1,877 | 2,828 | min | optimal 3 |
| hrc__exp1-0-10 | assignment-location | 691 | 691 | 610 | min | optimal 8 |
| hrc__exp1-1-5670 | assignment-location | 1,732 | 1,732 | 1,878 | min | optimal 2 |
| hrc__exp1-1-945 | assignment-location | 2,158 | 2,158 | 2,317 | min | optimal 11 |
| hrc__exp2-1-4795 | assignment-location | 5,407 | 5,407 | 5,658 | min | optimal 5 |
| hrc__exp2-1-5180 | assignment-location | 6,272 | 6,272 | 6,484 | min | optimal 5 |
| is__A3PZaPjnUz | other | 9,791 | 9,791 | 1,640 | min | optimal 103936 |
| is__jZ9pQqRxJ2 | other | 3,007 | 3,007 | 1,325 | min | optimal 210944 |
| java-auto-gen__binpack_11 | configuration | 2,223 | 2,223 | 3,497 | min | optimal 3 |
| java-auto-gen__pizza_8_3 | configuration | 3,156 | 3,156 | 4,635 | min | optimal 20 |
| java-auto-gen__plusexample_6 | configuration | 118 | 118 | 105 | min | optimal -43 |
| java-auto-gen__projplan1_15_15 | configuration | 1,114 | 1,114 | 1,758 | min | optimal 5 |
| java-auto-gen__routing_5 | configuration | 3,673 | 3,673 | 7,088 | min | feasible 69 |
| java-routing__trip_6_3 | routing | 3,177 | 3,177 | 1,952 | min | unknown |
| java-routing__trip_7_1 | routing | 4,709 | 4,709 | 2,655 | min | unknown |
| java-routing__trip_7_2 | routing | 4,695 | 4,695 | 2,654 | min | unknown |
| java-routing__trip_8_1 | routing | 6,629 | 6,629 | 3,418 | min | unknown |
| java-routing__trip_8_5 | routing | 6,615 | 6,615 | 3,420 | min | unknown |
| jobshop2__la03 | scheduling | 511 | 511 | 736 | min | feasible 619 |
| jobshop2__la04 | scheduling | 511 | 511 | 736 | min | optimal 590 |
| jobshop2__la05 | scheduling | 511 | 511 | 736 | min | optimal 593 |
| jobshop2__mt06 | scheduling | 223 | 223 | 313 | min | optimal 55 |
| jobshop2__mt10 | scheduling | 1,011 | 1,011 | 1,461 | min | feasible 964 |
| jobshop__jobshop_la06 | scheduling | 1,126 | 1,126 | 1,650 | min | feasible 926 |
| jobshop__jobshop_la22 | scheduling | 2,251 | 2,251 | 3,300 | min | feasible 999 |
| jobshop__jobshop_la36 | scheduling | 3,376 | 3,376 | 4,950 | min | feasible 1484 |
| jobshop__jobshop_orb06 | scheduling | 1,001 | 1,001 | 1,450 | min | feasible 1045 |
| jobshop__jobshop_vw3x3 | scheduling | 28 | 28 | 36 | min | optimal 256 |
| jp-encoding__data100 | other | 3,603 | 3,603 | 3,261 | min | optimal 5338 |
| jp-encoding__data200 | other | 5,010 | 5,010 | 4,426 | min | optimal 7544 |
| jp-encoding__data300 | other | 6,863 | 6,863 | 6,177 | min | optimal 11224 |
| kakuro__kakuro_6_6_easy | puzzle | 113 | 113 | 98 | sat | solved |
| kakuro__kakuro_6_6_hard | puzzle | 112 | 112 | 107 | sat | solved |
| kakuro__kakuro_6_6_super | puzzle | 120 | 120 | 112 | sat | solved |
| kakuro__kakuro_8_8_hard | puzzle | 210 | 210 | 186 | sat | solved |
| kakuro__kakuro_8_8_super | puzzle | 257 | 257 | 221 | sat | solved |
| knights__08_04 | puzzle | 280 | 280 | 118 | sat | solved |
| knights__08_10 | puzzle | 772 | 772 | 328 | sat | solved |
| knights__08_12 | puzzle | 936 | 936 | 398 | sat | solved |
| knights__08_14 | puzzle | 1,100 | 1,100 | 468 | sat | solved |
| langford__l_2_03 | design | 39 | 39 | 39 | sat | solved |
| langford__l_2_06 | design | 141 | 141 | 78 | sat | unsat |
| langford__l_2_12 | design | 534 | 534 | 156 | sat | solved |
| langford__l_2_18 | design | 1,179 | 1,179 | 234 | sat | unsat |
| langford__l_2_24 | design | 2,076 | 2,076 | 312 | sat | solved |
| latin-squares__03 | puzzle | 36 | 36 | 36 | sat | solved |
| latin-squares__07 | puzzle | 392 | 392 | 196 | sat | solved |
| latin-squares__10 | puzzle | 1,100 | 1,100 | 400 | sat | solved |
| latin-squares__12 | puzzle | 1,872 | 1,872 | 576 | sat | solved |
| latin-squares__15 | puzzle | 3,600 | 3,600 | 900 | sat | solved |
| league__model10-3-4 | rostering-timetabling | 195 | 195 | 168 | min | optimal 39992 |
| league__model40-5-12 | rostering-timetabling | 2,057 | 2,057 | 1,844 | min | optimal 139965 |
| league__model55-3-12 | rostering-timetabling | 2,069 | 2,069 | 1,672 | min | optimal 109949 |
| league__model60-5-11 | rostering-timetabling | 3,151 | 3,151 | 2,850 | min | optimal 149958 |
| league__model70-16-3 | rostering-timetabling | 3,949 | 3,949 | 3,542 | min | feasible 259971 |
| ma-path-finding__ins_simple | routing | 3,963 | 3,963 | 3,717 | min | optimal 25 |
| magicseq__005 | puzzle | 35 | 35 | 15 | sat | solved |
| magicseq__010 | puzzle | 120 | 120 | 30 | sat | solved |
| magicseq__020 | puzzle | 440 | 440 | 60 | sat | solved |
| magicseq__030 | puzzle | 960 | 960 | 90 | sat | solved |
| magicseq__040 | puzzle | 1,680 | 1,680 | 120 | sat | solved |
| mapping__mesh2x2_1 | assignment-location | 422 | 422 | 416 | min | optimal 1000 |
| mapping__mesh3x3_2 | assignment-location | 980 | 980 | 882 | min | optimal 900 |
| mapping__mesh3x3_mp3 | assignment-location | 1,938 | 1,938 | 1,691 | min | optimal 933 |
| mapping__mesh3x3_mpeg_2 | assignment-location | 3,734 | 3,734 | 3,330 | min | optimal 905 |
| mapping__ring_2 | assignment-location | 932 | 932 | 876 | min | optimal 1940 |
| mario__mario_easy_2 | routing | 579 | 579 | 1,251 | max | optimal 628 |
| mario__mario_easy_5 | routing | 579 | 579 | 1,251 | max | optimal 445 |
| mario__mario_medium_1 | routing | 2,049 | 2,049 | 4,731 | max | optimal 1481 |
| mario__mario_n_medium_1 | routing | 2,049 | 2,049 | 4,731 | max | optimal 1062 |
| mario__mario_n_medium_5 | routing | 2,049 | 2,049 | 4,731 | max | optimal 771 |
| market_split__s3-01 | packing-cutting | 20 | 20 | 3 | sat | solved |
| market_split__s5-05 | packing-cutting | 40 | 40 | 5 | sat | unknown |
| market_split__u3-06 | packing-cutting | 20 | 20 | 3 | sat | unsat |
| market_split__u4-01 | packing-cutting | 30 | 30 | 4 | sat | unknown |
| market_split__u5-10 | packing-cutting | 40 | 40 | 5 | sat | unknown |
| maximum-dag__15_05 | graph | 142 | 142 | 205 | max | optimal 46 |
| maximum-dag__25_01 | graph | 231 | 231 | 337 | max | optimal 71 |
| maximum-dag__25_04 | graph | 227 | 227 | 330 | max | optimal 70 |
| maximum-dag__25_06 | graph | 265 | 265 | 393 | max | optimal 80 |
| maximum-dag__31_02 | graph | 280 | 280 | 407 | max | optimal 89 |
| mqueens__n11 | puzzle | 1,777 | 1,777 | 7,013 | min | optimal 5 |
| mqueens__n12 | puzzle | 2,173 | 2,173 | 8,943 | min | optimal 7 |
| mrcpsp__mm_j10_j10_54_7 | scheduling | 4,924 | 4,924 | 9,605 | min | optimal 21 |
| mrcpsp__mm_m1_m1_53_6 | scheduling | 3,110 | 3,110 | 1,811 | min | optimal 65 |
| mrcpsp__mm_n0_n0_1_2 | scheduling | 5,315 | 5,315 | 9,315 | min | optimal 15 |
| mrcpsp__mm_n0_n0_1_6 | scheduling | 5,678 | 5,678 | 9,969 | min | optimal 23 |
| multi-knapsack__mknap1-6 | packing-cutting | 50 | 50 | 6 | sat | solved |
| multi-knapsack__mknap2-10 | packing-cutting | 105 | 105 | 3 | sat | solved |
| multi-knapsack__mknap2-2 | packing-cutting | 60 | 60 | 31 | sat | solved |
| multi-knapsack__mknap2-31 | packing-cutting | 70 | 70 | 6 | sat | solved |
| multi-knapsack__mknap2-32 | packing-cutting | 80 | 80 | 6 | sat | solved |
| nfc__12_2_10 | other | 24 | 24 | 25 | min | optimal 848 |
| nfc__12_2_5 | other | 23 | 23 | 25 | min | optimal 1074 |
| nfc__18_3_5 | other | 35 | 35 | 37 | min | optimal 1338 |
| nfc__24_4_10 | other | 48 | 48 | 49 | min | optimal 1912 |
| nfc__bockmayr_12hr | other | 12 | 12 | 13 | min | optimal 438 |
| nmseq__020 | puzzle | 420 | 420 | 60 | sat | solved |
| nmseq__040 | puzzle | 1,640 | 1,640 | 120 | sat | solved |
| nmseq__060 | puzzle | 3,660 | 3,660 | 180 | sat | solved |
| nmseq__099 | puzzle | 9,900 | 9,900 | 297 | sat | unknown |
| nmseq__83 | puzzle | 6,972 | 6,972 | 249 | sat | solved |
| nonogram__dom_06 | puzzle | 1,541 | 1,541 | 2,349 | sat | solved |
| nonogram__dom_08 | puzzle | 2,877 | 2,877 | 4,213 | sat | solved |
| nonogram__dom_10 | puzzle | 4,629 | 4,629 | 6,621 | sat | solved |
| nonogram__dom_12 | puzzle | 6,797 | 6,797 | 9,573 | sat | solved |
| nonogram__non_micro | puzzle | 109 | 109 | 220 | sat | solved |
| nsp__period_14_56 | rostering-timetabling | 1,722 | 1,722 | 1,866 | sat | solved |
| nsp__period_14_84 | rostering-timetabling | 2,142 | 2,142 | 2,322 | sat | solved |
| nsp__period_28_69 | rostering-timetabling | 4,284 | 4,284 | 4,884 | sat | solved |
| nsp__period_28_98 | rostering-timetabling | 4,284 | 4,284 | 4,884 | sat | solved |
| nsp__test | rostering-timetabling | 172 | 172 | 140 | sat | solved |
| on-call-rostering__10s-150d | rostering-timetabling | 3,053 | 3,053 | 2,733 | min | optimal 5 |
| on-call-rostering__10s-50d | rostering-timetabling | 1,427 | 1,427 | 1,559 | min | optimal 0 |
| on-call-rostering__20s-200d | rostering-timetabling | 7,883 | 7,883 | 6,502 | min | optimal 2 |
| on-call-rostering__4s-10d | rostering-timetabling | 179 | 179 | 227 | min | optimal 1 |
| on-call-rostering__4s-23d | rostering-timetabling | 390 | 390 | 440 | min | optimal 2 |
| open_stacks__problem_10_20_1 | sequencing | 2,631 | 2,631 | 1,683 | min | feasible 7 |
| open_stacks__tiny | sequencing | 496 | 496 | 368 | min | optimal 3 |
| open_stacks__wbo_30_15_1 | sequencing | 4,047 | 4,047 | 3,477 | min | feasible 10 |
| open_stacks__wbop_20_10_1 | sequencing | 1,541 | 1,541 | 1,611 | min | optimal 8 |
| open_stacks__wbop_30_10_1 | sequencing | 2,211 | 2,211 | 2,351 | min | feasible 14 |
| openshop__gp10-4 | scheduling | 2,801 | 2,801 | 4,600 | min | optimal 1077 |
| openshop__j7per10-1 | scheduling | 932 | 932 | 1,519 | min | optimal 1000 |
| openshop__j8per0-2 | scheduling | 1,409 | 1,409 | 2,304 | min | optimal 1052 |
| opt-cryptanalysis__r4 | other | 6,753 | 6,753 | 769 | min | optimal 12 |
| opt-cryptanalysis__r5 | other | 8,433 | 8,433 | 961 | min | optimal 20 |
| p1f__4 | design | 209 | 209 | 245 | min | optimal 28 |
| p1f__6 | design | 1,334 | 1,334 | 1,361 | min | optimal 80 |
| p1f__7 | design | 2,624 | 2,624 | 2,582 | min | unsat |
| p1f__9 | design | 7,739 | 7,739 | 7,280 | min | unsat |
| parity-learning__44_22_5.2 | other | 264 | 264 | 217 | min | optimal 2 |
| parity-learning__44_22_5.3 | other | 259 | 259 | 197 | min | optimal 2 |
| parity-learning__48_24_6.3 | other | 290 | 290 | 245 | min | unknown |
| parity-learning__52_26_6.1 | other | 312 | 312 | 257 | min | optimal 5 |
| parity-learning__52_26_6.3 | other | 307 | 307 | 237 | min | optimal 1 |
| pattern-set-mining__anneal-k1 | other | 503 | 503 | 1,039 | max | optimal 494 |
| pentominoes__01 | puzzle | 2,588 | 2,588 | 1,592 | sat | solved |
| photo__photo1 | assignment-location | 198 | 198 | 247 | max | optimal 10 |
| photo__photo2 | assignment-location | 261 | 261 | 295 | max | optimal 12 |
| prize-collecting__15-3-5-1 | routing | 608 | 608 | 738 | max | optimal 24 |
| prize-collecting__20-4-5-7 | routing | 1,013 | 1,013 | 1,188 | max | optimal 62 |
| prize-collecting__25-5-5-6 | routing | 1,518 | 1,518 | 1,738 | max | optimal 79 |
| prize-collecting__28-4-7-4 | routing | 1,869 | 1,869 | 2,116 | max | optimal 58 |
| prize-collecting__32-4-8-9 | routing | 2,393 | 2,393 | 2,676 | max | optimal 77 |
| project-planning__ProjectPlannertest_12_6 | scheduling | 2,694 | 2,694 | 4,681 | min | feasible 17 |
| project-planning__ProjectPlannertest_13_8 | scheduling | 3,158 | 3,158 | 5,529 | min | feasible 25 |
| project-planning__ProjectPlannertest_15_7 | scheduling | 4,197 | 4,197 | 7,446 | min | feasible 57 |
| project-planning__ProjectPlannertest_16_8 | scheduling | 4,772 | 4,772 | 8,521 | min | optimal 29 |
| project-planning__ProjectPlannertest_17_9 | scheduling | 5,384 | 5,384 | 9,674 | min | feasible 48 |
| prop_stress__0100 | synthetic | 202 | 202 | 5,251 | sat | unsat |
| QCP__qcp-10-67-0_ext | puzzle | 737 | 737 | 334 | sat | solved |
| QCP__qcp-15-120-0_ext | puzzle | 1,920 | 1,920 | 690 | sat | solved |
| QCP__qcp-20-187-0_ext | puzzle | 3,927 | 3,927 | 1,174 | sat | solved |
| QCP__qcp-20-187-9_ext | puzzle | 3,927 | 3,927 | 1,174 | sat | solved |
| QCP__qcp-25-264-9_ext | puzzle | 6,864 | 6,864 | 1,778 | sat | solved |
| quasigroup7__05 | puzzle | 139 | 139 | 474 | sat | solved |
| quasigroup7__06 | puzzle | 237 | 237 | 832 | sat | unsat |
| quasigroup7__07 | puzzle | 372 | 372 | 1,334 | sat | unsat |
| quasigroup7__09 | puzzle | 777 | 777 | 2,866 | sat | unknown |
| quasigroup7__12 | puzzle | 1,812 | 1,812 | 6,844 | sat | unknown |
| queens__004 | puzzle | 20 | 20 | 34 | sat | solved |
| queens__008 | puzzle | 90 | 90 | 166 | sat | solved |
| queens__020 | puzzle | 588 | 588 | 1,138 | sat | solved |
| queens__050 | puzzle | 3,723 | 3,723 | 7,348 | sat | solved |
| radiation__01 | assignment-location | 691 | 691 | 708 | min | optimal 370 |
| radiation__04 | assignment-location | 1,019 | 1,019 | 1,047 | min | optimal 636 |
| radiation__07 | assignment-location | 1,146 | 1,146 | 1,173 | min | optimal 487 |
| radiation__i6-11 | assignment-location | 1,400 | 1,400 | 1,425 | min | optimal 895 |
| radiation__i7-15 | assignment-location | 2,467 | 2,467 | 2,502 | min | optimal 1308 |
| rcpsp-max__psp_j10_33 | scheduling | 1,847 | 1,847 | 1,456 | min | optimal 70 |
| rcpsp-max__psp_j20_34 | scheduling | 1,385 | 1,385 | 3,071 | min | feasible 95 |
| rcpsp-max__psp_j20_35 | scheduling | 1,428 | 1,428 | 3,199 | min | feasible 103 |
| rcpsp-max__psp_j30_123 | scheduling | 3,178 | 3,178 | 7,080 | min | feasible 153 |
| rcpsp-max__psp_j30_33 | scheduling | 3,027 | 3,027 | 6,749 | min | feasible 119 |
| rcpsp-wet__j30_1_3-wet | scheduling | 3,088 | 3,088 | 1,792 | min | optimal 93 |
| rcpsp-wet__j30_35_9-wet | scheduling | 4,326 | 4,326 | 2,651 | min | optimal 104 |
| rcpsp-wet__j30_4_8-wet | scheduling | 3,935 | 3,935 | 2,352 | min | optimal 83 |
| rcpsp-wet__j60_19_6-wet | scheduling | 9,939 | 9,939 | 5,563 | min | optimal 227 |
| rcpsp-wet__j60_36_8-wet | scheduling | 9,699 | 9,699 | 5,345 | min | optimal 336 |
| rcpsp__data_ksd15_d_j3028_10 | scheduling | 614 | 614 | 1,462 | min | optimal 533 |
| rcpsp__data_ksd15_d_j3034_5 | scheduling | 164 | 164 | 373 | min | optimal 513 |
| rcpsp__data_pack_pack007 | scheduling | 1,939 | 1,939 | 1,267 | min | optimal 41 |
| rcpsp__data_psplib_j30_J30_11_9 | scheduling | 2,582 | 2,582 | 6,093 | min | optimal 67 |
| rcpsp__data_psplib_j30_J30_41_3 | scheduling | 2,805 | 2,805 | 6,353 | min | optimal 85 |
| rectangle-packing__data_square_rpp03_false | packing-cutting | 11 | 11 | 8 | sat | solved |
| rectangle-packing__data_square_rpp03_true | packing-cutting | 60 | 60 | 66 | sat | solved |
| rectangle-packing__data_square_rpp10_true | packing-cutting | 1,453 | 1,453 | 1,052 | sat | solved |
| rectangle-packing__data_square_rpp15_false | packing-cutting | 4,170 | 4,170 | 2,723 | sat | solved |
| rectangle-packing__data_square_rpp25_true | packing-cutting | 7,179 | 7,179 | 8,241 | sat | unknown |
| road-cons__road_11 | scheduling | 4,491 | 4,491 | 8,277 | min | optimal 5020 |
| road-cons__road_8 | scheduling | 1,219 | 1,219 | 2,165 | min | feasible 5875 |
| road-cons__road_9 | scheduling | 1,977 | 1,977 | 3,566 | min | optimal 3206 |
| schur_numbers__10-3 | design | 225 | 225 | 278 | sat | solved |
| schur_numbers__5-3 | design | 50 | 50 | 58 | sat | solved |
| schur_numbers__7-3 | design | 107 | 107 | 129 | sat | solved |
| search_stress2__02_07 | synthetic | 43 | 43 | 56 | sat | unsat |
| search_stress__04_04 | synthetic | 54 | 54 | 74 | sat | unsat |
| search_stress__08_04 | synthetic | 106 | 106 | 146 | sat | unsat |
| search_stress__08_08 | synthetic | 346 | 346 | 562 | sat | unknown |
| ship-schedule__3Ships | scheduling | 2,675 | 2,675 | 4,324 | max | optimal 265650 |
| ship-schedule__3ShipsMixedUnconst | scheduling | 2,592 | 2,592 | 4,221 | max | optimal 172500 |
| ship-schedule__4ShipsMixed | scheduling | 3,398 | 3,398 | 5,476 | max | optimal 191750 |
| ship-schedule__6Ships | scheduling | 5,295 | 5,295 | 8,531 | max | optimal 607220 |
| ship-schedule__7ShipsUnconst | scheduling | 6,194 | 6,194 | 9,979 | max | optimal 699750 |
| shortest_path__00 | routing | 217 | 217 | 65 | min | optimal 88 |
| shortest_path__01 | routing | 256 | 256 | 64 | min | optimal 42 |
| shortest_path__02 | routing | 465 | 465 | 129 | min | optimal 59 |
| shortest_path__08 | routing | 513 | 513 | 129 | min | optimal 144 |
| shortest_path__09 | routing | 1,025 | 1,025 | 257 | min | optimal 549 |
| slow_convergence__0200 | synthetic | 102 | 102 | 1,325 | sat | solved |
| smelt__smelt_2 | scheduling | 646 | 646 | 1,603 | min | optimal 69 |
| smelt__smelt_3 | scheduling | 3,355 | 3,355 | 8,789 | min | optimal 1117 |
| smelt__smelt_4 | scheduling | 973 | 973 | 2,462 | min | optimal 1043 |
| solbat__sb_12_12_5_0 | puzzle | 4,691 | 4,691 | 8,620 | sat | solved |
| solbat__sb_12_12_5_1 | puzzle | 4,691 | 4,691 | 8,620 | sat | unknown |
| solbat__sb_12_12_5_2 | puzzle | 4,691 | 4,691 | 8,620 | sat | unknown |
| solbat__sb_12_12_6_1 | puzzle | 4,908 | 4,908 | 9,895 | sat | solved |
| solbat__sb_12_12_6_4 | puzzle | 4,908 | 4,908 | 9,895 | sat | solved |
| spot5__1502 | scheduling | 3,983 | 3,983 | 1,054 | min | optimal 28042 |
| spot5__29 | scheduling | 2,779 | 2,779 | 1,305 | min | optimal 8059 |
| spot5__503 | scheduling | 5,959 | 5,959 | 1,849 | min | optimal 11113 |
| spot5__54 | scheduling | 2,228 | 2,228 | 770 | min | optimal 37 |
| steiner-triples__07 | design | 576 | 576 | 1,021 | sat | solved |
| steiner-triples__09 | design | 1,614 | 1,614 | 3,180 | sat | unknown |
| still-life-wastage__09 | design | 2,131 | 2,131 | 2,933 | max | optimal 43 |
| still-life-wastage__10 | design | 2,637 | 2,637 | 3,648 | max | optimal 54 |
| still-life-wastage__11 | design | 3,197 | 3,197 | 4,441 | max | optimal 64 |
| still-life-wastage__12 | design | 3,811 | 3,811 | 5,312 | max | unknown |
| still-life-wastage__13 | design | 4,479 | 4,479 | 6,261 | max | unknown |
| still_life2__still_life_5 | design | 448 | 448 | 330 | max | optimal 16 |
| still_life2__still_life_6 | design | 653 | 653 | 477 | max | optimal 18 |
| still_life2__still_life_7 | design | 896 | 896 | 650 | max | optimal 28 |
| still_life2__still_life_9 | design | 1,496 | 1,496 | 1,074 | max | feasible 39 |
| still_life__2x4 | design | 141 | 141 | 105 | max | optimal 6 |
| still_life__3x8 | design | 457 | 457 | 323 | max | optimal 12 |
| still_life__4x4 | design | 301 | 301 | 213 | max | optimal 8 |
| still_life__8x8 | design | 1,277 | 1,277 | 853 | max | feasible 36 |
| still_life__9x9 | design | 1,626 | 1,626 | 1,078 | max | feasible 24 |
| stochastic-fjsp__fjsp-a1-s2_fjsp-t15-j3-m3-a1_det | scheduling | 800 | 800 | 1,078 | min | optimal 108 |
| stochastic-fjsp__fjsp-a1-s3_fjsp-t20-j4-m3-a1_det | scheduling | 1,918 | 1,918 | 2,651 | min | optimal 207 |
| stochastic-fjsp__fjsp-a1-s4_fjsp-t8-j2-m3-a1_det | scheduling | 283 | 283 | 397 | min | optimal 242 |
| stochastic-fjsp__fjsp-a1-s5_fjsp-t8-j2-m3-a1_det | scheduling | 342 | 342 | 489 | min | optimal 328 |
| stochastic-fjsp__fjsp-a1-s6_fjsp-t8-j2-m3-a1_det | scheduling | 393 | 393 | 573 | min | optimal 348 |
| stochastic-vrp__vrp-s2-v2-c7_vrp-v2-c7_det | routing | 894 | 894 | 2,051 | min | optimal 160 |
| stochastic-vrp__vrp-s3-v2-c6_vrp-v2-c6_det | routing | 1,048 | 1,048 | 2,386 | min | optimal 194 |
| stochastic-vrp__vrp-s3-v2-c7_vrp-v2-c7_det | routing | 1,337 | 1,337 | 3,076 | min | optimal 230 |
| stochastic-vrp__vrp-s4-v2-c6_vrp-v2-c6_det | routing | 1,395 | 1,395 | 3,181 | min | optimal 221 |
| stochastic-vrp__vrp-s5-v2-c8_vrp-v2-c8_det | routing | 2,764 | 2,764 | 6,426 | min | optimal 330 |
| sugiyama__g3_7_7_7 | graph | 512 | 512 | 883 | min | optimal 4 |
| sugiyama__g4_7_7_7_3 | graph | 595 | 595 | 1,019 | min | feasible 7 |
| sugiyama__g4_7_7_7_7 | graph | 753 | 753 | 1,297 | min | feasible 15 |
| sugiyama__g5_7_7_7_7_2 | graph | 794 | 794 | 1,362 | min | feasible 13 |
| sugiyama__g5_7_7_7_7_3 | graph | 826 | 826 | 1,425 | min | feasible 16 |
| table-layout__en-1000-1286-line764 | assignment-location | 3,365 | 3,365 | 2,318 | min | optimal 4501 |
| table-layout__en-1000-1407-line1350 | assignment-location | 1,026 | 1,026 | 407 | min | optimal 1040 |
| table-layout__en-1250-1303-line283 | assignment-location | 8,206 | 8,206 | 1,406 | min | optimal 2345 |
| table-layout__en-1250-1407-line976 | assignment-location | 1,881 | 1,881 | 805 | min | optimal 1707 |
| table-layout__en-1250-1479-line1633 | assignment-location | 4,531 | 4,531 | 1,465 | min | optimal 2970 |
| talent_scheduling__easy_concert | sequencing | 295 | 295 | 458 | min | optimal 89 |
| talent_scheduling__easy_small | sequencing | 139 | 139 | 224 | min | optimal 36 |
| talent_scheduling__medium_film103 | sequencing | 1,112 | 1,112 | 1,630 | min | feasible 969 |
| talent_scheduling__medium_film118 | sequencing | 941 | 941 | 1,155 | min | feasible 824 |
| talent_scheduling__medium_MobStory | sequencing | 1,661 | 1,661 | 1,758 | min | feasible 1063 |
| tc-graph-color__k10_31 | graph | 2,401 | 2,401 | 4,036 | min | optimal 427 |
| tc-graph-color__k10_34 | graph | 2,464 | 2,464 | 4,171 | min | optimal 433 |
| tc-graph-color__k10_41 | graph | 2,557 | 2,557 | 4,354 | min | unknown |
| tc-graph-color__k5_05 | graph | 1,535 | 1,535 | 2,568 | min | optimal 273 |
| tc-graph-color__k9_39 | graph | 2,371 | 2,371 | 3,988 | min | optimal 481 |
| template_design__catfood_2 | packing-cutting | 181 | 181 | 338 | min | optimal 418 |
| template_design__catfood_3 | packing-cutting | 275 | 275 | 496 | min | optimal 408 |
| template_design__herbs_2 | packing-cutting | 2,797 | 2,797 | 5,517 | min | unknown |
| template_design__herbs_3 | packing-cutting | 4,199 | 4,199 | 8,222 | min | unknown |
| template_design__magazine_inserts_2 | packing-cutting | 4,413 | 4,413 | 8,716 | min | unknown |
| tents__tents_1 | puzzle | 29 | 29 | 44 | sat | solved |
| tents__tents_2 | puzzle | 52 | 52 | 77 | sat | solved |
| tents__tents_3 | puzzle | 206 | 206 | 305 | sat | solved |
| tpp__tpp_3_3_20_1 | routing | 499 | 499 | 940 | min | optimal 126 |
| tpp__tpp_5_3_20_1 | routing | 967 | 967 | 1,966 | min | optimal 141 |
| tpp__tpp_5_5_20_1 | routing | 2,067 | 2,067 | 4,476 | min | optimal 115 |
| tpp__tpp_6_3_30_1 | routing | 1,465 | 1,465 | 3,004 | min | optimal 164 |
| tpp__tpp_7_5_30_1 | routing | 3,947 | 3,947 | 8,716 | min | optimal 124 |
| train__instance.1 | scheduling | 1,340 | 1,340 | 2,645 | min | optimal 6630 |
| train__instance.12 | scheduling | 2,752 | 2,752 | 5,376 | min | feasible 77760 |
| train__instance.13 | scheduling | 2,752 | 2,752 | 5,376 | min | feasible 78700 |
| train__instance.5 | scheduling | 2,758 | 2,758 | 5,398 | min | feasible 78350 |
| train__instance.9 | scheduling | 2,756 | 2,756 | 5,391 | min | feasible 80600 |
| traveling-tppv__circ8abal | routing | 4,797 | 4,797 | 2,730 | min | feasible 98 |
| traveling-tppv__circ8bbal | routing | 4,797 | 4,797 | 2,730 | min | feasible 92 |
| traveling-tppv__circ8cbal | routing | 4,797 | 4,797 | 2,730 | min | optimal 78 |
| traveling-tppv__circ8dbal | routing | 4,797 | 4,797 | 2,730 | min | feasible 94 |
| traveling-tppv__circ8ebal | routing | 4,797 | 4,797 | 2,730 | min | feasible 90 |
| triangular__n10 | design | 56 | 56 | 496 | max | optimal 20 |
| triangular__n16 | design | 137 | 137 | 3,061 | max | feasible 35 |
| trucking__01 | routing | 25 | 25 | 16 | min | optimal 220 |
| trucking__05 | routing | 36 | 36 | 19 | min | optimal 287 |
| trucking__10 | routing | 1,001 | 1,001 | 298 | min | optimal 1736 |
| trucking__12 | routing | 201 | 201 | 58 | min | optimal 245 |
| trucking__14 | routing | 301 | 301 | 88 | min | optimal 580 |
| trucking_hl__trucking_hl_1 | routing | 25 | 25 | 16 | min | optimal 220 |
| trucking_hl__trucking_hl_2 | routing | 25 | 25 | 11 | min | optimal 210 |
| trucking_hl__trucking_hl_3 | routing | 25 | 25 | 16 | min | optimal 224 |
| trucking_hl__trucking_hl_4 | routing | 33 | 33 | 22 | min | optimal 324 |
| trucking_hl__trucking_hl_5 | routing | 36 | 36 | 13 | min | optimal 287 |
| vrp__A-n33-k6.vrp | routing | 1,090 | 1,090 | 1,059 | min | feasible 771 |
| vrp__A-n38-k5.vrp | routing | 1,445 | 1,445 | 1,409 | min | feasible 812 |
| vrp__A-n61-k9.vrp | routing | 3,722 | 3,722 | 3,663 | min | feasible 1253 |
| vrp__P-n16-k8.vrp | routing | 257 | 257 | 243 | min | optimal 450 |
| vrp__P-n50-k10.vrp | routing | 2,501 | 2,501 | 2,453 | min | feasible 786 |
| zephyrus__12__6__6__3 | configuration | 2,886 | 2,886 | 5,315 | min | optimal 780 |
| zephyrus__12__6__8__3 | configuration | 2,964 | 2,964 | 5,357 | min | optimal 1300 |
| zephyrus__12__8__6__3 | configuration | 2,904 | 2,904 | 5,329 | min | optimal 1300 |
| zephyrus__14__10__8__3 | configuration | 3,860 | 3,860 | 7,229 | min | optimal 2600 |
| zephyrus__14__8__6__3 | configuration | 3,776 | 3,776 | 7,185 | min | optimal 1170 |
