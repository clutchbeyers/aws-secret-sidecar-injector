FROM amazonlinux
COPY ./admission-controller /admission-controller
RUN chmod 700 /admission-controller
ENTRYPOINT ["/admission-controller"]
