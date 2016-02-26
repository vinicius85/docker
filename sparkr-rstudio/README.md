### RStudio Server + SparkR Docker Container

Container intended to run RStudio with SparkR, based on [Rocker Rstudio image](https://hub.docker.com/r/rocker/rstudio/).


#### Getting started

```
docker pull vinicius85/sparkr-rstudio
``` 

You can also pull source code or fork project for adding more R packages in `setup.R` and install them at docker image build time


#### Usage

```
docker run -dt -p 8787:8787 vinicius85/sparkr-rstudio
```

Default versions: Spark 1.6.0 with Hadoop 2.6. SPARK_VERSION and HADOOP_VERSION can be overwritten using Docker `--env` parameter

If you need some code example, you can check [SparkR MLlib Logistic Regression example](http://rpubs.com/tcosta/sparkr-glm) for first insights.