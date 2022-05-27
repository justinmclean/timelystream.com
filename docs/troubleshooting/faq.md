---
title: Frequently Asked Questions
---


### Who makes DuckDB?
DuckDB is maintained by [Dr. Mark Raasveldt](https://mytherin.github.io) & [Dr. Hannes Mühleisen](https://hannes.muehleisen.org) along with [many other contributors](https://github.com/duckdb/duckdb/graphs/contributors) from all over the world. Mark and Hannes have set up the [DuckDB Foundation](https://duckdb.org/foundation/) that collects donations and funds development and maintenance of DuckDB. Mark and Hannes are also co-founders of [DuckDB Labs](https://www.duckdblabs.com), which provides commercial services around DuckDB. Several other DuckDB contributors are also affiliated with DuckDB Labs.  
DuckDB's initial development took place at the [Database Architectures Group](https://www.cwi.nl/research/groups/database-architectures) at the [Centrum Wiskunde & Informatica (CWI)](https://www.cwi.nl) in Amsterdam, The Netherlands. 

### Why call it DuckDB?
Ducks are amazing animals. They can fly, walk and swim. They can also live off pretty much everything. They are quite resilient to environmental challenges. A duck's song will bring people back from the dead and [inspires database research](https://static1.squarespace.com/static/51f8f4aae4b0cdf15da554e1/57023acae321408302d6b936/5973b537bebafb04b9520c3d/1500755312736/11_Wilbur_buiten_DQ1C0104.jpg?format=1000w). They are thus the perfect mascot for a versatile and resilient data management system. Also the logo designs itself.

### Where do I find the DuckDB Logo?
You can download the DuckDB Logo here: <br/> • Web: [png](/images/logo-dl/DuckDB_Logo.png) / [jpg](/images/logo-dl/DuckDB_Logo.jpg) <br/>  • Print: [svg](/images/logo-dl/DuckDB_Logo.svg) / [pdf](/images/logo-dl/DuckDB_Logo.pdf) <br/><br/>The DuckDB logo & website were designed by [Jonathan Auch](http://jonathan-auch.de) & [Max Wohlleber](https://maxwohlleber.de).

### How can I expand the DuckDB website?
The DuckDB Website is hosted by GitHub pages, its repository is [here](
https://github.com/duckdb/duckdb-web). Pull requests to fix issues or generally expand the documentation section are very welcome.

### I benchmarked DuckDB and its slower than \[some other system\]
In a departure from traditional academic systems research practise, we have at first focused our attention on correctness, not raw performance. So it is entirely possible DuckDB is slower than some other, more mature system at this point. That being said, we are now confident DuckDB produces correct query results, and are actively working to make it fast, too. So publishing benchmark numbers from the current preview releases is certainly interesting, but should not be taken as the definitive results on what the DuckDB architecture can or cannot do.

### Does DuckDB use SIMD
DuckDB does not use *explicit SIMD* instructions because they greatly complicate portability and compilation. Instead, DuckDB uses *implicit SIMD*, where we go to great lengths to write our C++ code in such a way that the compiler can *auto-generate SIMD instructions* for the specific hardware. As an example why this is a good idea, porting DuckDB to the new Apple M1 architecture took 10 minutes.


