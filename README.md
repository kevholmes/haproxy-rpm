# haproxy 1.5-dev branch RPM spec

* Tested on CentOS/RHEL 6.x x86_64

## This is a modified version of the spec pulled from the source tarball available at:

* http://http://haproxy.1wt.eu/

## Default compile options

* USE_PCRE=1 TARGET=linux26 ARCH=x86_64 USE_OPENSSL=1 USE_ZLIB=1

### How do?

	$ sudo yum install -y rpm-build rpmdevtools pcre-devel openssl-devel zlib-devel redhat-rpm-config gcc gcc-c++ make libstdc++-devel
	$ rpmdev-setuptree

	$ git clone https://github.com/kevholmes/haproxy-rpm.git
	$ cp haproxy-rpm/haproxy.spec ~/rpmbuild/SPECS/
	$ rpmbuild -vv -ba ~/rpmbuild/SPECS/haproxy.spec
	$ cd ~/rpmbuild/RPMS/x86_64/
	$ sudo yum install haproxy-1.5-devX.x86_64.rpm

