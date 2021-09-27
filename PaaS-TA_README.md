## gorouter-gos 적용(CVE: HTTP Basic Authentication Enabled)
```
$ git clone  https://github.com/PaaS-TA/routing-release -b 0.207.0-PaaS-TA-v2.2
$ cd routing-release
$ git submodule sync --recursive && git submodule foreach --recursive git submodule sync  && git submodule update --init --recursive
$ cd  src/
$ cp gorouter-gos/basic_auth.go  code.cloudfoundry.org/gorouter/common/http/basic_auth.go
$ bosh create-release ...
```
