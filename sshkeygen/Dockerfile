FROM sshclient
RUN echo "ssh-keygen -t rsa -f id_rsa -N ''" > genkey
RUN echo "clear" >> genkey
RUN echo "cat id_rsa" >> genkey
RUN echo "cat id_rsa.pub" >> genkey
CMD ["sh","genkey"]