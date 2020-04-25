# NYC 311 Complaints Exploration

<img src="nyc311-logo.png" width="300">


### Setup

As pre-work, ensure that you have both [`Docker`](https://docs.docker.com/install/) and [`Docker Compose`](https://docs.docker.com/compose/install/) installed on your machine.

```bash
$ git clone https://github.com/jamespooley/nyc_311_complaints.git
$ cd nyc_311_complaints
```

To builds, (re)create, start, and attach to the container in order to reproduce the analyses, enter the following in your terminal:

```bash
$ docker-compose down && docker-compose build --no-cache && docker-compose up --force-recreate
```

Once the terminal says that the container is up and running, do the following:

* Enter http://localhost:8888 in your browser
* Navigate to the `01_data_ingest_clean.ipynb` notebook and run all cells. The notebook sources, cleans, and explores the data.
* Once all the cells in the previous notebook run, open `02_data_explore.ipynb` and execute all cells. This notebook answers certain questions about the 311 data.
* Note that `00_data_ingest_explore.ipynb` is not intended to be run, and simply records my thinking when getting used to the data. In other words, this is exploratory pre-work before arriving at `01_data_ingest_clean.ipynb`.

Once the code in the two notebooks has been executed, destroy the container by entering:

```bash
$ docker-compose down
```

in your terminal.

Note that this project (currently) only uses one service (viz., the Jupyter notebooks with the analyses),
so the use of Docker Compose is overkill here, as no real orchestration of containers for 
nubmerous services is needed.


### Further Reading and Exploration

* [Running a Containter](https://jupyter-docker-stacks.readthedocs.io/en/latest/using/running.html) from the Jupyter Docker Stacks documentation
* Johnson, S. (2010). [What a Hundred Million Calls to 311 Reveal about New York](https://www.wired.com/2010/11/ff_311_new_york/). _Wired_
* [The Promises and Pitfalls of 311 Data](https://arwhite.mit.edu/promises-pitfalls-311-data) in _Urban Affairs Review_
* [Docker Compose for Data Science](https://www.andrewmahon.info/blog/docker-compose-data-science)
* [311 Service Requests from 2010 to Present](https://data.cityofnewyork.us/Social-Services/311-Service-Requests-from-2010-to-Present/erm2-nwe9)
* [Analyzing 311 Complaints per Tract and Merging Data with Census Analysis](https://github.com/BuzzFeedNews/2018-06-nyc-311-complaints-and-gentrification/blob/master/notebooks/03-311-call-nyc-analysis.ipynb)
* [Geographic Areas Reference Manual](https://www.census.gov/programs-surveys/geography/guidance/geographic-areas-reference-manual.html) from the United States Census Bureau
* [US Census Bureau Geographic Entities and Concepts](https://www.census.gov/content/dam/Census/data/developers/geoareaconcepts.pdf)
* [Securely Storing Credentials in a Jupyter Notebook](http://veekaybee.github.io/2020/02/25/secrets/)
