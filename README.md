# haproxy 1.5-dev branch RPM spec

* Tested on CentOS/RHEL 6.x x86_64

### What is this? 

* Spec file included with haproxy source finds itself causing trouble with CentOS / RHEL.

### Default compile options

* USE_PCRE=1 TARGET=linux26 ARCH=x86_64 USE_OPENSSL=1 USE_ZLIB=1

### How do?

	$ sudo yum install -y rpm-build rpmdevtools pcre-devel openssl-devel zlib-devel redhat-rpm-config gcc gcc-c++ make libstdc++-devel
	$ rpmdev-setuptree

	$ git clone https://github.com/kevholmes/haproxy-rpm.git
	$ cp haproxy-rpm/haproxy.spec ~/rpmbuild/SPECS/
	$ rpmbuild -vv -ba ~/rpmbuild/SPECS/haproxy.spec
	$ cd ~/rpmbuild/RPMS/x86_64/
	$ sudo yum install haproxy-1.5-devX.x86_64.rpm

