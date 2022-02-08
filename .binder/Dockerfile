FROM rocker/binder:3.6.0
LABEL maintainer='James Tripp'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}
RUN wget https://github.com/WarwickCDI/workshop-introductory-social-media-analysis-R/raw/main/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2019-09-09/')); devtools::install_deps()"
