# Papers

This repository stores paper that motivates the project. 

[An Empirical Evaluation of Columnar Storage Formats](/columnar.pdf) gives a nice illustration of how apache parquet is structured and the argument for implementing additional auxillary data structures (disk speed is catching up and the bottleneck is shifting to compute, so it might be worth reading more structrues from disk in exchange for faster compute)

[Column Sketch](/sketches.pdf) presents the core data structure and algorithm we want to reproduce and extend in the project. In one sentance is is an order-preserving compression to allow scanning only on compressed values. The performance argument is that scanning is bottlenecked by memory bandwith, and by accessing smaller memory per value we can perform scan faster.