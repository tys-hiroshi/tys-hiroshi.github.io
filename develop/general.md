## DBのSELECT,UPDATE など

DBのSELECT,UPDATE などに失敗した場合(例えば、TIMEOUT)を考慮して、実装する。
Retryする、複数件UPDATEする場合は、失敗したものをエラーとして処理をすすめるかなど。

