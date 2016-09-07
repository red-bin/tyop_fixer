Uses difflib to link typos and condensed street names to an opencv list of addresses. Only tried for street names, since including address types, numbers and dirs created false positives. Corrects around half of typos.

I'll try to add some smarter regression stuffs eventually.

```
$ wc -l corrected.csv badstreets | wc -l | head -2
  9259 corrected.csv
 22555 badstreets
```

```
$ cat corrected.csv | sort -R | head -30
ssndburg,sandburg,0.875
prominitory,promontory,0.857142857143
nowark,newark,0.833333333333
fletchef,fletcher,0.875
kostner al,kostner,0.823529411765
sheridan rr,sheridan,0.842105263158
pulsk,pulaski,0.833333333333
loral,lorel,0.8
philipps,phillips,0.875
soak,oak,0.857142857143
cleven,cleveland,0.8
caliifornia,california,0.952380952381
ogesby,oglesby,0.923076923077
burkham,burnham,0.857142857143
harmpden,hampden,0.933333333333
nort,north,0.888888888889
rdige,ridge,0.8
coumbia,columbia,0.933333333333
argy,argyle,0.8
menomee,menomonee,0.875
newladn,newland,0.857142857143
boulevard way,boulevard,0.818181818182
sherwn,sherwin,0.923076923077
lawrencec,lawrence,0.941176470588
kildale,kildare,0.857142857143
illinios,illinois,0.875
archev,archer,0.833333333333
lawrace,lawrence,0.8
armitate,armitage,0.875
racibe,racine,0.833333333333
```
