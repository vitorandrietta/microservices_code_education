FROM golang as base
WORKDIR /var/opt
COPY main.go /var/opt
RUN go build main.go


FROM scratch
WORKDIR /var/opt
COPY --from=base /var/opt/main .

ENTRYPOINT [ "./main" ]

