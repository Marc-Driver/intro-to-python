# intro-to-python
+ Code
+ Text
[ ]
+ Code
+ Text
[ ]
print("Hello World")
[10]
Hello World
+ Code
+ Text
Variables
+ Code
+ Text
[ ]
age = 20
print(age)
[11]
20
+ Code
+ Text
Practice: Change the value of age and print it out in the following space.

+ Code
+ Text
[ ]
+ Code
+ Text
Deep Dive: different types of variables.

+ Code
+ Text
[ ]
age = 20
price = 19.99 
first_name = "Mr. Doe"
is_online = True
print(first_name + " is " + str(age) + " years old")
[13]
Mr. Doe is 20 years old
+ Code
+ Text
Exercise: Check in a new patient named James Smith, who is 20 years old.

+ Code
+ Text
[ ]
+ Code
+ Text
Input

+ Code
+ Text
[ ]
name = input("what is your name")
print("Hello " + name)
[15]
Hello Marc
+ Code
+ Text

+ Code
+ Text
Type conversion

+ Code
+ Text
Error: the input is read in as a string, which cannot be operated on with a number.
+ Code
+ Text
[ ]
birth_year = input("Enter your birth year")
age = 2021 - int(birth_year)
print (age)
[16]
23
+ Code
+ Text
Fixing the code: convert string input to integer

+ Code
+ Text
[ ]
birth_year = input("Enter your birth year")
age = 2021 - int(birth_year)
print (age)
[17]
23
+ Code
+ Text
Exercise: Basic calculator. Adding two numbers

+ Code
+ Text
[ ]
first = input ("First: ")
second = input ("Second: ")
sum = int(first) + int(second)
print("Sum: " + str(sum))
[18]
Sum: 30
+ Code
+ Text
Strings

+ Code
+ Text
[ ]
# The string class contains a lot of built-in methods
course = 'Discover AI'
print (course.upper())
print (course.lower())
print ('Discover' in course)
print(course.find('i'))
[38]
DISCOVER AI
discover ai
True
1
+ Code
+ Text
Operators
+ Code
+ Text
Arthmetic Operators
+ Code
+ Text
[ ]
# Addition
print("10 + 3 = " + str(10 + 3))

# Subtraction
print("10 - 3 = " + str(10 - 3))

# Multiplication
print("10 * 3 = " + str(10 * 3))

# Division

[39]
10 + 3 = 13
10 - 3 = 7
10 * 3 = 30
10 / 3 = 3.3333333333333335
10 //3 = 3
10 % 3 = 1
10 ** 3 = 1000
+ Code
+ Text
[ ]
# Augmented operators
x = 10
x += 3
print(x)
[21]
13
+ Code
+ Text
Operator Precedence

+ Code
+ Text
[ ]
x = 10 + 3 * 2
print (x)
[22]
16
+ Code
+ Text
Comparison Operators
+ Code
+ Text
[ ]
# They return boolean (True/False) solutions

# Greater than
print("10 > 3: " + str(10 > 3))
# Greater than or equal to
print("3 >= 3: " + str(10 >= 3))
# Less than
print("10 < 3: " + str(10 < 3))
# Less than or equal to
print("10 <= 3: " + str(10 <= 3))

[23]
10 > 3: True
3 >= 3: True
10 < 3: False
10 <= 3: False
10 == 3: False
10 != 3: True
+ Code
+ Text
Logical Operators
+ Code
+ Text
[ ]
# Used for building complex rules and conditions

# Using "and" check that a price is between two values
price = 25
print("Price between 10 and 30: " + str(price > 10 and price < 30))

# Using "or" check that a price is either of two values
price = 25
print("Price is either 10 or 30: " + str(price == 10 or price == 30))


[24]
Price between 10 and 30: True
Price is either 10 or 30: False
Price is less than 30: False
+ Code
+ Text
If Statements
+ Code
+ Text
[ ]
# Used to make decisions

# Print a message if the temperature is > 30
temperature = 35
if(temperature > 30):
    print("It's a hot day")
    print("Drink plenty of water")
# Everything below will be outside of the conditional statement
print ("Done")
[25]
It's a hot day
Drink plenty of water
Done
+ Code
+ Text
Practice Add a condition for printing "It's a nice day" if the temperature is between 20 and 30

+ Code
+ Text
[ ]
temperature = 25
if(temperature > 30):
    print("It's a hot day")
    print("Drink plenty of water")
if (temperature > 20 and temperature < 30):
    print ("It's a nice day")
[44]
It's a nice day
+ Code
+ Text
Exercise

Get weight as input
Get unit as input (Kgs or Lbs)
Display weight converted to the opposite unit
+ Code
+ Text
[ ]
weight = int(input("Weight: "))
unit = input ("(K)g or (L)bs: ")
if unit.upper() == "K":
    converted = weight / 0.45
    print ("Weight in Lbs: " + str(converted))
else:
    converted = weight * 0.45
    print ("Weight in Kgs: " + str(converted))
[49]
Weight in Kgs: 103.5
+ Code
+ Text
Loops
+ Code
+ Text
[ ]
i = 1
while i <= 1000:
    print(i)
    i = i + 1


1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
51
52
53
54
55
56
57
58
59
60
61
62
63
64
65
66
67
68
69
70
71
72
73
74
75
76
77
78
79
80
81
82
83
84
85
86
87
88
89
90
91
92
93
94
95
96
97
98
99
100
101
102
103
104
105
106
107
108
109
110
111
112
113
114
115
116
117
118
119
120
121
122
123
124
125
126
127
128
129
130
131
132
133
134
135
136
137
138
139
140
141
142
143
144
145
146
147
148
149
150
151
152
153
154
155
156
157
158
159
160
161
162
163
164
165
166
167
168
169
170
171
172
173
174
175
176
177
178
179
180
181
182
183
184
185
186
187
188
189
190
191
192
193
194
195
196
197
198
199
200
201
202
203
204
205
206
207
208
209
210
211
212
213
214
215
216
217
218
219
220
221
222
223
224
225
226
227
228
229
230
231
232
233
234
235
236
237
238
239
240
241
242
243
244
245
246
247
248
249
250
251
252
253
254
255
256
257
258
259
260
261
262
263
264
265
266
267
268
269
270
271
272
273
274
275
276
277
278
279
280
281
282
283
284
285
286
287
288
289
290
291
292
293
294
295
296
297
298
299
300
301
302
303
304
305
306
307
308
309
310
311
312
313
314
315
316
317
318
319
320
321
322
323
324
325
326
327
328
329
330
331
332
333
334
335
336
337
338
339
340
341
342
343
344
345
346
347
348
349
350
351
352
353
354
355
356
357
358
359
360
361
362
363
364
365
366
367
368
369
370
371
372
373
374
375
376
377
378
379
380
381
382
383
384
385
386
387
388
389
390
391
392
393
394
395
396
397
398
399
400
401
402
403
404
405
406
407
408
409
410
411
412
413
414
415
416
417
418
419
420
421
422
423
424
425
426
427
428
429
430
431
432
433
434
435
436
437
438
439
440
441
442
443
444
445
446
447
448
449
450
451
452
453
454
455
456
457
458
459
460
461
462
463
464
465
466
467
468
469
470
471
472
473
474
475
476
477
478
479
480
481
482
483
484
485
486
487
488
489
490
491
492
493
494
495
496
497
498
499
500
501
502
503
504
505
506
507
508
509
510
511
512
513
514
515
516
517
518
519
520
521
522
523
524
525
526
527
528
529
530
531
532
533
534
535
536
537
538
539
540
541
542
543
544
545
546
547
548
549
550
551
552
553
554
555
556
557
558
559
560
561
562
563
564
565
566
567
568
569
570
571
572
573
574
575
576
577
578
579
580
581
582
583
584
585
586
587
588
589
590
591
592
593
594
595
596
597
598
599
600
601
602
603
604
605
606
607
608
609
610
611
612
613
614
615
616
617
618
619
620
621
622
623
624
625
626
627
628
629
630
631
632
633
634
635
636
637
638
639
640
641
642
643
644
645
646
647
648
649
650
651
652
653
654
655
656
657
658
659
660
661
662
663
664
665
666
667
668
669
670
671
672
673
674
675
676
677
678
679
680
681
682
683
684
685
686
687
688
689
690
691
692
693
694
695
696
697
698
699
700
701
702
703
704
705
706
707
708
709
710
711
712
713
714
715
716
717
718
719
720
721
722
723
724
725
726
727
728
729
730
731
732
733
734
735
736
737
738
739
740
741
742
743
744
745
746
747
748
749
750
751
752
753
754
755
756
757
758
759
760
761
762
763
764
765
766
767
768
769
770
771
772
773
774
775
776
777
778
779
780
781
782
783
784
785
786
787
788
789
790
791
792
793
794
795
796
797
798
799
800
801
802
803
804
805
806
807
808
809
810
811
812
813
814
815
816
817
818
819
820
821
822
823
824
825
826
827
828
829
830
831
832
833
834
835
836
837
838
839
840
841
842
843
844
845
846
847
848
849
850
851
852
853
854
855
856
857
858
859
860
861
862
863
864
865
866
867
868
869
870
871
872
873
874
875
876
877
878
879
880
881
882
883
884
885
886
887
888
889
890
891
892
893
894
895
896
897
898
899
900
901
902
903
904
905
906
907
908
909
910
911
912
913
914
915
916
917
918
919
920
921
922
923
924
925
926
927
928
929
930
931
932
933
934
935
936
937
938
939
940
941
942
943
944
945
946
947
948
949
950
951
952
953
954
955
956
957
958
959
960
961
962
963
964
965
966
967
968
969
970
971
972
973
974
975
976
977
978
979
980
981
982
983
984
985
986
987
988
989
990
991
992
993
994
995
996
997
998
999
1000
+ Code
+ Text
Lists
+ Code
+ Text
[ ]
# list of names
names = ["Jane", "John", "Mary", "Sam", "Safi"]
print(names[1])
names[0] = "Jon"
print (names[0:3])
# print the first three names

# Add a name at the head of the list
[54]
John
['Jon', 'John', 'Mary']
+ Code
+ Text
List methods

+ Code
+ Text
[ ]
numbers = [1, 2, 3, 4, 5, 6]
# Append
numbers.append(6)
print (numbers)
# Insert
numbers.insert(0,-1)
print (numbers)
# Remove
numbers.remove(3)
print (numbers)

[60]
[1, 2, 3, 4, 5, 6, 6]
[-1, 1, 2, 3, 4, 5, 6, 6]
[-1, 1, 2, 4, 5, 6, 6]
False
0
+ Code
+ Text
For Loops
+ Code
+ Text
[ ]
numbers = [1, 2, 3, 4, 5,]
for item in numbers:
    print (item)

i=0
while i < len(numbers):  
    print(numbers[i])
    i += 1  
[61]
1
2
3
4
5
1
2
3
4
5
+ Code
+ Text
Range function

+ Code
+ Text
[ ]
# The function can have 1 to 3 arguments.

# 1. generate numbers up to a value
numbers = range(5, 10 ,2)
for number in numbers:
    print(number)
[62]
5
7
9
+ Code
+ Text
Tuples

+ Code
+ Text
[ ]
# Immutable (unchangeable) elements
numbers = (1, 2, 3)
numbers.count(3)
[63]
1
