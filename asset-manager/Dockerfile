FROM ruby:2.6.3
RUN apt-get update -qq && apt-get upgrade -y && apt-get install -y build-essential clamav vim
RUN freshclam
RUN ln -sf /usr/bin/clamscan /usr/bin/govuk_clamscan

RUN useradd -m build
USER build

ENV EDITOR=vim
