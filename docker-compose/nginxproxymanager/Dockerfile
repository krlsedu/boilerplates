FROM jc21/nginx-proxy-manager:latest
RUN apt-get update && apt-get install -y
RUN sh <(curl -sSf https://downloads.nordcdn.com/apps/linux/install.sh) -n
RUN nordvpn login --token 771799848f02d22a220c7b5d324c4819ab15d3ae37574785dd369fa885e2f848
RUN nordvpn set meshnet on