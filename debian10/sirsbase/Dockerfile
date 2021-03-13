FROM kathara/base:debian10

ARG DEBIAN_FRONTEND="noninteractive"
RUN apt update
RUN apt upgrade -y

# Install nemesis:
RUN curl -sS https://deb.troglobit.com/pubkey.gpg | apt-key add -
RUN echo "deb [arch=amd64] https://deb.troglobit.com/debian stable main" | tee /etc/apt/sources.list.d/troglobit.list

RUN apt update 
RUn apt install -y nemesis

RUN apt install -y nmap \
                   telnetd \
                   libdnet-dev \
                   libpcap-dev \
                   exim4 \
                   openvpn \
                   man