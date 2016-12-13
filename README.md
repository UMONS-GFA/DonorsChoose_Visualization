# DonorsChoose_Visualization
* Source Code for my blog post: [Interactive Data Visualization with D3.js, DC.js, Python, and MongoDB](http://adilmoujahid.com/posts/2015/01/interactive-data-visualization-d3-dc-python-mongodb/)

#Visit my Blog : http://adilmoujahid.com

## Getting started

The dependencies for the project can be installed using

    $ pip install -r requirements.txt

You can use ``Vagrant`` to start a machine with a MongoDB instance running

    $ vagrant up

To initialize the database you need to download the data

    $ wget http://s3.amazonaws.com/open_data/opendata_projects000.gz && gzip -d opendata_projects000.gz
    
If download is broken, you can download projects data on this [page](https://research.donorschoose.org/t/download-opendata/33)

Don't forget to give extension file

    $ gzip -d opendata_projects000.gz && mv opendata_projects000 opendata_projects000.csv


and import it

    $ mongoimport -d donorschoose -c projects --type csv --headerline /PATH/TO/DATA/opendata_projects000.csv
