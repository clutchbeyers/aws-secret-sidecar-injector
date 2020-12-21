FROM amazonlinux
COPY ./admission-controller /admission-controller
RUN chmod 777 -R /admission-controller
ENTRYPOINT ["/admission-controller"]
