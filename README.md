# ietf-115-tdd
Supporting materials for the IETF 115 TDD on QUIC

## Example of a good exchange on localhost

Using Cloudflare quiche quiche-client and quiche-server example apps:

* quiche-server --no-retry
* quiche-client --no-verify --wire-version 1 https://127.0.0.1:4433/index.html

logs:

* localhost-good.pcapng
* client-localhost-good.sqlog
* server-localhost-good.sqlog

## Example of incorrect transport parameters for HTTP/3 on localhost

* quiche-server --no-retry
* SSLKEYLOGFILE=tdd.keys QLOGDIR=qlogs quiche-client --no-verify --wire-version 1 –-max-streams-uni 0 https://127.0.0.1:4433/index.html

logs:

* localhost-0-streams-uni.pcapng
* client-localhost-0-streams-uni.sqlog
* server-localhost-0-streams-uni.sqlog

## Example of incorrect transport parameters for HTTP/3 on localhost

* quiche-server --no-retry
* SSLKEYLOGFILE=tdd.keys QLOGDIR=qlogs quiche-client --no-verify --wire-version 1 –-max-streams-uni 0 https://lucaspardue.com/index.html

logs:

* localhost-0-streams-uni.pcapng
* client-lucaspardue.com-0-streams-uni.sqlog
* server-lucaspardue.com-0-streams-uni.sqlog
