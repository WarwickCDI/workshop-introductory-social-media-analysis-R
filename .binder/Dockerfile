FROM ghcr.io/jamestripp/cdi-intro-social_media-image:main
LABEL maintainer='James Tripp'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}