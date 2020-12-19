FROM amazonlinux
COPY ./admission-controller /admission-controller
RUN chmod +x -R /admission-controller
ENTRYPOINT ["/admission-controller"]
