FROM confluentinc/cp-zookeeper:latest
ENV ZK_USER=zookeeper \
ZOOKEEPER_CLIENT_PORT=2181


#Copy configuration generator script to bin
COPY scripts /opt/zookeeper/bin/


RUN set -x \    
    && groupadd -g 1000 $ZK_USER \
    && useradd -r -u 1000 -g $ZK_USER $ZK_USER \
    && chown -R "$ZK_USER:$ZK_USER" /etc/kafka/ /var/lib/zookeeper /var/log/kafka

USER $ZK_USER