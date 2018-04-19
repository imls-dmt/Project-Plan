FROM jupyter/datascience-notebook

MAINTAINER Karl Benedict <kbene@unm.edu>

USER root


# Full Pandoc & Latex Environment
RUN wget https://github.com/jgm/pandoc/releases/download/1.19.1/pandoc-1.19.1-1-amd64.deb
RUN dpkg -i pandoc-1.19.1-1-amd64.deb
RUN apt-get update && \
	apt-get purge texlive && \
	apt-get install -y --no-install-recommends \
	texlive

## Taskjuggler and Ruby
RUN apt-get update && \
	apt-get purge ruby && \
	apt-get install -y --no-install-recommends \
	ruby
RUN gem install taskjuggler

USER jovyan
