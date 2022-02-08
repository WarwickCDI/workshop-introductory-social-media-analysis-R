FROM rocker/binder:4.2.0
LABEL maintainer='James Tripp'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}
# Install R packages
RUN install2.r --error \
    ggplot2 \
    knitr \
    lubridate \
    RedditExtractoR \
    rmarkdown \
    rtweet \
    tidytext \
    tidyverse

#RUN wget https://github.com/WarwickCDI/workshop-introductory-social-media-analysis-R/raw/main/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2019-09-09/')); options(install.packages.check.source = 'no'); devtools::install_deps()"
