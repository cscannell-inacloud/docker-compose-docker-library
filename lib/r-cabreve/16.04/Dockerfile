FROM r-base:16.04

RUN apt-get update \
        && apt-get install -y --no-install-recommends \
		pandoc \
		r-cran-yaml \
		r-cran-reshape2 \
		r-cran-plyr \
		r-cran-visnetwork \
		r-cran-igraph \
		r-cran-diagrammer \
 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds \
 	&& rm -rf /var/lib/apt/lists/*


VOLUME /source
WORKDIR /source
