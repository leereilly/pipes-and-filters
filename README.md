Pipes and Filters
=================

In software engineering, a pipeline consists of a chain of processing elements (processes, threads, coroutines, etc..), arranged so that the output of each element is the input of the next. Usually some amount of buffering is provided between consecutive elements. The information that flows in these pipelines is often a stream of records, bytes or bits. The concept is also called the pipes and filters design pattern [[WikiPedia](http://en.wikipedia.org/wiki/Pipeline_%28software%29)].

Overview
--------
The Pipe and Filter architecture is an architectural design pattern, where the system is comprised of a data sources, filters, pipes and data sinks (described below).

### Pipes
Pipes (or Pipelines) are the connectors; they link data sources to the first filter, between filters, be\As needed, a pipe synchronizes the active elements that it connects together.

### Filters
Filters are the processing units of the pipeline. A filter simply processes (and likely transforms) input data. Filters can be active or passive.

* Active filters run as a separate process or thread; it actively pulls data from the input data stream and pushes the transformed data onto the output data stream.
* Passive filters are activated by either being called as a function, a pull of the output from the filter or as a procedure, a push of output data into the filter.

### Data Sources
Data sources provide the input data to the system either by 
* actively pushing data down the pipeline or 
* passively supplying data when requested.

### Data Sinks
Data sinks gather data at the end of a pipeline either by
* actively pulling data from the last filter or
* passively responding when requested by the last filter.

Usage
-----