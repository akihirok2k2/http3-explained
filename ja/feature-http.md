## HTTP/3

HTTP レイヤは HTTP に準拠したトランスポートを行います。HTTP ヘッダ圧縮では QPACK を利用しており、
これは HTTP/2 における HPACK によく似ています。

HPACKアルゴリズムはストリームが順番に届くことを前提としているため、修正せずに HTTP/3 で再利用することは不可能です。
これは QUIC の提供するストリームにおいては伝送がばらばらに行われるためです。
QPACK は [HPACK](https://httpwg.org/specs/rfc7541.html) の QUIC 対応版といえます。