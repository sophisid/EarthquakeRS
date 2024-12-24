FROM alpine:3.4
ARG app
# Create apps folder

RUN mkdir /apps

COPY assets /apps/${app}/assets
COPY config /apps/${app}/config
COPY data /apps/${app}/data
COPY plugin.properties /apps/${app}/plugin.properties


RUN chown -R 100:101 /apps/
VOLUME /apps/${app}
CMD ["/bin/sh"]