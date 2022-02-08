FROM rocker/binder:3.5.3
LABEL maintainer='James Tripp'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}

RUN R -e "install.packages('knitr',dependencies=TRUE, repos='http://cran.rstudio.com/')"
RUN R -e "install.packages('lubridate',dependencies=TRUE, repos='http://cran.rstudio.com/')"
RUN R -e "install.packages('RedditExtractoR',dependencies=TRUE, repos='http://cran.rstudio.com/')"
RUN R -e "install.packages('rmarkdown',dependencies=TRUE, repos='http://cran.rstudio.com/')"
RUN R -e "install.packages('rtweet',dependencies=TRUE, repos='http://cran.rstudio.com/')"
RUN R -e "install.packages('tidytext',dependencies=TRUE, repos='http://cran.rstudio.com/')"

#RUN wget https://github.com/WarwickCDI/workshop-introductory-social-media-analysis-R/raw/main/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2019-09-09/')); options(install.packages.check.source = 'no'); devtools::install_deps()"
