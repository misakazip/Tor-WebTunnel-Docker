This repository was cloned from [gitlab.torproject.org](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/webtunnel).This is NOT official project.DO NOT seek supprt to Tor Project Forum about issues of the docker images. Some files were modified by [GitHub Actions script](https://github.com/misakazip/Tor-WebTunnel-Docker/blob/main/.github/workflows/sync_from_gitlab.yml).
# WebTunnel

Pluggable Transport based on HTTP Upgrade(HTTPT)

WebTunnel is pluggable transport that attempt to imitate web browsing activities based on [HTTPT](https://censorbib.nymity.ch/#Frolov2020b).

## Client Usage
Connect to a WebTunnel server with a Tor configuration file like:
```
UseBridges 1
DataDirectory datadir

ClientTransportPlugin webtunnel exec ./client

Bridge webtunnel 192.0.2.3:1 url=https://akbwadp9lc5fyyz0cj4d76z643pxgbfh6oyc-167-71-71-157.sslip.io/5m9yq0j4ghkz0fz7qmuw58cvbjon0ebnrsp0

SocksPort auto

Log info
```
## Running a WebTunnel Bridge

You can help censored users connect to the Tor network by running a WebTunnel bridge, see our [community documentation](https://community.torproject.org/relay/setup/webtunnel/) for more details.
