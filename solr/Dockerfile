FROM solr:7.3.0

ENV WEBAPP_BASE_PATH "/opt/solr/server/solr-webapp/webapp/WEB-INF/lib"

COPY --chown=$SOLR_USER:$SOLR_USER security.json /opt/solr/security.json
COPY --chown=$SOLR_USER:$SOLR_USER ci-start.sh /opt/solr/server/scripts/ci-start.sh

USER $SOLR_USER
