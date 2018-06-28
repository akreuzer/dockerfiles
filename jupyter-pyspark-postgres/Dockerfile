FROM jupyter/pyspark-notebook

USER root

ADD https://jdbc.postgresql.org/download/postgresql-42.2.2.jar /usr/local/spark/jars
RUN chmod a+r /usr/local/spark/jars/*

USER $NB_UID
